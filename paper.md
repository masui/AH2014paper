# Using BabaScript for Integrating Computer and Human Activities

## Abstract

We introduce the "BabaScript" programming system that supports
the integration of human and computer activities.
Although many recent programming systems support croudsourcing features
where computer programs can utilize human resources in the whole world,
computer resources and human resources are not fully integrated in
most of the systems.
Using the BABAScript system, all the computer activities and
human activities can be described in a powerful and simple
programming language, and
all the intelligent entities in the real world connected to the Internet
can be programmed in a consistent way.

<!--
人間をシステムの一部として扱える[[クラウドソーシング]]シス テムが最近流行している
 しかし人間をセンサとして利用できないなど、完全に対等になっていない
 人間と機械を完全に同等に扱えるスクリプト言語[[BABAScript]]を提案する
 [[BABAScript]]でいろんな面白いことが可能になる
 -->
 
## Introduction

Computer programs have long been widely used for
controling the behaviors of machines, but
human activities have not been described in the same
programming language style.
Although all the computers and devices in the whole world
are now going to be connected to the Internet and
controlled by a variety of software written in
various programming languages,
human behaviors and human tasks have not been
described in programming language styles, despite the fact that
human task descriptions are often described in similar styles.
For example, cooking recipes resemble programming languages
because they describe the order of tasks which 
people should follow for preparing foods.

For example, a recipe for preparing pasta should look like this:

	boil (a pan of water)
	put (some salt)
	wait (until water is hot enough)
	put (pasta into boild water)
	wait (10 minutes)

Here, a condition statment and a sleep statement is used
in the recipe, just like they are found in common program texts.
	
Job instructions can also be described in
program-like manner.
In a conference registration counter, people may be instructed
to work like this:

	while many people are waiting do
	  open all the registration counters
	end

The structure of these instructions are
similar to programming languages, but
computer languages and instructions for humans have been
used in different situations and environments, and they were
not treated as the same thing.

However, the two environments
are getting closer these days, because "crowdsoursing" has been
getting popular.
Many people are working on various research topics where
people can use human resources on the Web
as easily as using software libraries in computing systems.
For example,
users of a new word processor can use a croudsoursing
menu to ask people on the net to rewrite phrases,
just like
running a spell checker on the word processor[Miller].
In this case, there's little difference between
calling a spell checker and asking people on the
Net to rewite sentences.

These approaches are interesting because
distinctions between
computer resources and human resources are diminishing.
However, there still exist big differences between
computer functions and human functions, and
these systems are not flexible enough.
A computer program can get real-world sensing data on the net
using a sensor library,
but it cannot get similar data from people on the net,
since the method of getting data from sensors and
getting information from people are usually very different.
Similarly,
calling a system function and
asking people to do something are quite different.
If we can handle computer systems and people on the net
exactly the same way,
とても面白いことが起こると思われる。

People might like to have a laundry-taking system which can
execute a task like this:

    while true do
      if it's likely to rain then
        take in the laundry
      end
    end

We can use sensor devices or consult the Web to tell if
"it's likely to rain",
but we can also ask people if it is likely to rain or not.
We can use a special robot arm to take in the laundry,
while it would be easier to ask the family member to do the same thing.
In this way, 
either a machine or a human can sense data or perform action
in almost the same way, and
in some cases machines can do the job better than humens,
and in other cases humans are better at the job.

Simple household chores can be specified using
program-like descriptions.
If you have to prepare dinnaer at 19:00, 
you may have to behave like this:

- wash rice at 18:00
- put the rice into a pot with proper amount of water
- wait for 30 minutes
- put the pot on the gas stove with high flame
- set the heat low after hearing the boiling sound
- turn of the gas after 10 minites

Sensing the boiling sound is easy for humans, while simple 
sensing devices cannot detect whether the pot is heated enough.
Waiting for 10 minites is easy for computers, but that is
not easy for humans without using clocks.
For a very simple task like preparing rice,
collabolation between humans and computers is essential.
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
<!--  
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
   -->
  
  