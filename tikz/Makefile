TARGET :=
export

CLEAN_LIST := $(patsubst %.tex,%.idx,$(wildcard *.tex)) \
              $(patsubst %.tex,%.ind,$(wildcard *.tex)) \
              $(patsubst %.tex,%.dvi,$(wildcard *.tex)) \
              $(patsubst %.tex,%.pdf,$(wildcard *.tex)) \
              $(patsubst %.tex,%.log,$(wildcard *.tex)) \
              $(patsubst %.tex,%.aux,$(wildcard *.tex)) \
              $(patsubst %.tex,%.toc,$(wildcard *.tex)) \
              $(patsubst %.tex,%.snm,$(wildcard *.tex)) \
              $(patsubst %.tex,%.nav,$(wildcard *.tex)) \
              $(patsubst %.tex,%.out,$(wildcard *.tex))


build :
ifndef TARGET
	@printf "\e[101m 'TARGET' variable does not set.. \e[0m \n"
	@${MAKE} error ERROR_MESSAGE="TARGET"
endif
# 索引
#   .tex => .idx
#   .idx => .ind
# pdf
#   .tex & .ind => .dvi => .pdf
	${MAKE} ${TARGET}.tex
	${MAKE} ${TARGET}.ind
	${MAKE} ${TARGET}.dvi
	${MAKE} ${TARGET}.pdf

%.idx : %.tex
	platex -kanji=utf8 ${TARGET}.tex

%.ind : %.idx
	mendex -s ${TARGET}.ist ${TARGET}.idx

%.dvi : %.tex %.ind
	platex -kanji=utf8 $<

%.pdf : %.dvi
	dvipdfmx $^

.phony : error
error :  ## errors処理を外部に記述することで好きなエラーメッセージをprintfで記述可能.
	$(error "${ERROR_MESSAGE}")

.phony : clean
clean :
	-rm -rf ${CLEAN_LIST}