# AH2014 Paper

## Abstract

We introduce the "BabaScript" system which can handle
software and humans in the same programming environment.


人間をシステムの一部として扱える[[クラウドソーシング]]シス テムが最近流行している
 しかし人間をセンサとして利用できないなど、完全に対等になっていない
 人間と機械を完全に同等に扱えるスクリプト言語[[BABAScript]]を提案する
 [[BABAScript]]でいろんな面白いことが可能になる
 
## Introduction

<!-- 言いたいことはパラグラフの最初に書くこと -->

Computer programs have long been widely used for
controling the behaviors of machines.
All the computers and devices in the whole world
are now connected on the Internet and
controlled by a variety of software written in
various programming languages.

On the other hand,
human behaviors and human tasks are not usually
described in programming languages, although
human task descriptions are in many cases described
in program-like languages.
For example, cooking recipes are very similar
to programming languages, since they describe
what people should do for preparing foods.

	boil(a pan of water)
	if(water is hot enough){
	   put pasta into boild water
	}
	
Job instructions can also be described in
program-like texts.

	while many people are waiting do
	  open all the レジ counters
	end

The structure of these instructions are
similar to computer programming languages, but
computer languages and instructions for humans have been
used in very different environments, and they were
not used together in the same environment.

However, the two different language environments
are getting closer, because "crowdsoursing" has been
getting popular recently.
Researchers are working on various reasearches where
people can use human resources on the Web
as easily as using software libraries in a system.
For example,
users of a word processor can easily use a croudsoursing
menu to ask people on the net to rewrite phrases,
just like
running a spell checker on the word processor[Miller].
In this case, there's little difference between
calling a spell checking library and asking people on the
Net to rewite sentences.

These approaches are interesting because
distinctions between
computer resources and human resources are diminishing.
However, there still exist big differences between
computer functions and human functions, and
these systems are not flexible enough.
<!-- 対等でない -->
A computer program can get a real-world sensing data on the net
using a sensor library,
but it cannot get similar data from people on the net,
since the method of getting data from sensors and
getting information from people are usually very different.
Similarly,
calling a software function and
asking people to do something are quite different.
If we can handle computer systems and people on the net
exactly the same way,
とても面白いことが起こると思われる。

People might like to have a laundry-taking system which can
execute a task like this:

    if it's likely to rain then
      take in the laundry
    end

We can use sensor devices or consult the Web to tell if
"it's likely to rain",
but we can also ask people if if it is likely to rain or not.
Also, we can use a special robot to take in the laundry,
while we can ask your family member to do the same thing.
In this way, 
either a machine or a human can sense data or perform action
in almost the same way.

Even household chores can be described using
program-like descriptions.
If you have to prepare a Japanese dinnaer at 19:00, 
you may have to behave like this:

- wash rice at 18:00
- put the rice in a pot with proper amount of water
- wait for 30 minutes
- put the pot on the gas stove with high flame
- set the heat low after hearing the boiling sound
- turn of the gas after 10 minites

Sensing the boiling sound is easy for humans, but simple sensors
cannot detect it.
Waiting for 10 minites is easy for computers, but that is
not easy for humans.
For a very simple task like preparing rice,
collabolation between humans and computers is quite effective.
<!-- センシングは人間がやる -->

While the user is waiting for the rice to be cooked,
he can do other tasks for the meal.
Such activities can be described using a programming language
which supports parallel processing.



<!--
  しかしこれらはまだ限定的であり、できないことも多い
   [[[ユーザと機械が対等でない]]]
	ユーザからの 要求に応じて 機械が 動く
	機械からの 要求に応じて 人間が 行動する
   ある時刻にベルをならす(=機械を動)ことはできるが人間を起こす(=人間を行動)ことはできない
   人間のセンサを条件にすることができない
	すごく主観的なものをプログラミングに記述できない
	if 綺麗な景色を見たら then とか
  人間のセンシング行動やアクションも含めて完全に融合したプログラミング環境があれば面白い!
  -->
  
 [[[例]]]
  [[[日常的な仕事の記述]]]
   [[[条件やアクションが人間でも機械でも同等]]]
   [[[if]]] 誰かいる [[[then]]] ドアを開ける
   [[[if]]] 雨がふる [[[then]]] 洗濯をとりこむ
   [[[if]]] 人が足りない [[[then]]] 応援を呼ぶ
   [[[if]]] Amazonが来た [[[then]]] メールする
   [[[if]]] ディスクが無い [[[then]]] 買う(Amazon/アキバ)
   [[[if]]] ビールが無い [[[then]]] 買う
   [[[if]]] 7時になる [[[then]]] 起きる
   7時になったらベルがなるのではなく 7時になったら起きる
   TODOリストとか目覚まし時計とかはプログラミングである
  [[[7時の夕食の用意]]]
   6時に米を洗う
   水と一緒に土鍋に入れて30分放置する
   火をつける
   [[[沸騰したら]]]弱火にする
   8分たったら火を止める
   その間に別の料理を用意する
   この場合、センサを人間がやってる (沸騰したら)
	if文の中身が人間のセンサ
   また並列プログラミングになってる
  [[[既存のシステムではこういう仕事をスクリプトとして記述することはできない]]]
  [[BABAScript]][[[だと楽勝]]]
   だとイイネ
 [[[方法 = プログラム上で人/コンピュータへの命令の区別をなくす]]]
  コンピュータのプログラムと人のプログラムが融合
   行動を人がやる場合と機械がやる場合 (action)
   条件を機械が認識する場合と人が認識する場合 (センサ/条件)
   どちらでも良い場合もある (e.g. 天気)
	「雨がふってきたら」は人間が判断しても機械判断でもよい
  人が得意なことや、人にしかできないことは人にやらせる
   現実のものを動かす
   人間だけが認識できるもの
	CAPTCHAとか
  コンピュータが得意なことはコンピュータにやらせる
   普通の計算とか
   モータを回すとか
  世の中のあらゆる手順や行動をプログラムとして記述する
  人間を機械と同じように記述できる
  
  綺麗な景色だと写真をとる
   みたいなことは人間にしかできない
  
  