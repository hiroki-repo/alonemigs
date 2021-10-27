---Japanese---
Alone MiGSを手に取っていただきありがとうございます。
このdllはhspのaxファイルをありとあらゆる言語から実行できるようにするものです。
使い方:
引数は2つ指定します。
fprocutil 
引数1:	0の場合は動的読み込みしたプログラムのアドレスを得るためのオプションになるため
	引数2にaxファイルのファイル名が入ったポインタを代入します。(amigs.asではsptrのため文字列指定でok)
	それ以外では引数1のポインタのプログラムを実行するので引数2に指定した値や
	文字列のポインタは実行するプログラムからはstatに見えます。
引数2:	ファイル名のポインタか実行する変換済みプログラムから見えるstatの値
例:
#include "amigs.as"
ptr4prg=fprocutil(0,"hello.ax")
mes fprocutil(ptr4prg,"")
---English---
Thank you for get the Alone MiGS dll module!
The dll can be used to execute hsp ax format immediate code from any programming language!
The way to use it:
You have to set 1 args.
Arg1:	If the arg is NULL, Arg2 should be set a pointer of the ax file's filename which being dynareced.(in amigs.as arg2 is sptr to use char)
	Else, Arg1 should be set an address of dynareced ax data and in the situation arg2 should be a value or pointer of stat at the relocated binary
	be to executed!
Arg2:	a pointer of ax file's filename or dynareced program's stat.
Example:
#include "amigs.as"
ptr4prg=fprocutil(0,"hello.ax")
mes fprocutil(ptr4prg,"")
---License---

OpenHSP

Copyright (C) 1997-2017, Onion Software/onitama.
All rights reserved.

ソースコード形式かバイナリ形式か、変更するかしないかを問わず、以下の条件を満たす場合に限り、再頒布および使用が許可されます。 

・ソースコードを再頒布する場合、上記の著作権表示、本条件一覧、および下記免責条項を含めること。 
・バイナリ形式で再頒布する場合、頒布物に付属のドキュメント等の資料に、上記の著作権表示、本条件一覧、および下記免責条項を含めること。 
・書面による特別の許可なしに、本ソフトウェアから派生した製品の宣伝または販売促進に、Onion Softwareの名前またはコントリビューターの名前を使用してはならない。 

本ソフトウェアは、著作権者およびコントリビューターによって「現状のまま」提供されており、明示黙示を問わず、商業的な使用可能性、および特定の目的に対する適合性に関する暗黙の保証も含め、またそれに限定されない、いかなる保証もありません。著作権者もコントリビューターも、事由のいかんを問わず、 損害発生の原因いかんを問わず、かつ責任の根拠が契約であるか厳格責任であるか（過失その他の）不法行為であるかを問わず、仮にそのような損害が発生する可能性を知らされていたとしても、本ソフトウェアの使用によって発生した（代替品または代用サービスの調達、使用の喪失、データの喪失、利益の喪失、業務の中断も含め、またそれに限定されない）直接損害、間接損害、偶発的な損害、特別損害、懲罰的損害、または結果損害について、一切責任を負わないものとします。 
