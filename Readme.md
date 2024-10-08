# 量子五目並べ

<!-- add video in assets dir -->

<p align="center">
  <img src="./assets/Comp_01.gif" width=90%>
</p>

## 概要
このリポジトリは、こちらの動画と同様のルールで量子五目並べを実装するリポジトリです。

[【理解不能】何色になるか分からない量子で五目並べやってみた【でも楽しそう】](https://www.youtube.com/watch?v=mitAxA3f4U4)


## ルール
### 基本ルール
- 基本的には五目並べと同じルール、黒 or 白が 5 つ並べたら勝ち
- 三三、四四、超連 などの禁じ手はない者とする
- 黒が先手、白が後手
- 白と黒の 1 ターンずつの手番が交互に行われる

### 量子ルール
- 各石には、その石が黒となる確率 (%) が表記されている
- 黒は 90%、70% の石を交互に打つ
- 白は 10%、30% の石を交互に打つ
- 「観測」という動作は、盤面の石の色を確定させる動作であり、「観測」をするまで石の色は確定しない
- 「観測」をして初めて石の色が確定され、勝敗判定に移る
- 勝敗判定の結果、黒 or 白が 5 つ並べられていない場合、元の石の確率に戻してゲームを続行する。
- ゲームが続行した場合、盤面の石は「観測」前の状態に戻り、確率表記となり、次回以降の観測には影響しない→ n 回目の「観測」時に黒であっても次以降の「観測」で黒になる保証はない
- 勝敗判定の結果、黒 or 白が 5 つ並べられている場合、その時点で 5 つ並んでいる側の勝利となり、ゲーム終了となる
- 「観測」によって、白と黒、両方の石が 5 つ並べられている場合、「観測」を行った側の勝利となる
- 盤面が全て埋まっても勝敗がつかない場合、引き分けとなる

## 実行方法
html ファイルを ダブルクリック で実行することができます。
ゲームをリセットする場合は F5 キーを押してください。

## プログラムの説明
[Gomoku.html](/Gomoku.html) は普通の五目並べのゲームです。
[quantaization_gomoku_vs_CPU_select_turn.html](/quantaization_gomoku_vs_CPU_select_turn.html) は量子五目並べのゲームです。対戦相手は CPU です。先手後手を選択できます。
[quantaization_gomoku_two_people.html](/quantaization_gomoku_two_people.html) は量子五目並べのゲームです。対戦相手はプレイヤーです。2 人または 1 人のシミュレーション用に作成されています。


## Overview
This repository is an implementation of quantum Gomoku with rules similar to this video.

[【理解不能】何色になるか分からない量子で五目並べやってみた【でも楽しそう】](https://www.youtube.com/watch?v=mitAxA3f4U4)

## Rules
### Basic rules
- Basically the same rules as Gomoku, win if you line up 5 black or white stones
- There are no forbidden moves such as 3-3, 4-4, and super-connection
- Black goes first, white goes second
- Black and white take turns playing one turn at a time

### Quantum rules
- Each stone is marked with the probability (%) that the stone will be black
- Black plays 90% and 70% stones alternately
- White plays 10% and 30% stones alternately
- The operation called "observation" is an operation that determines the color of the stones on the board, and the color of the stones is not determined until the "observation" is made
- Once the "observation" is made, the color of the stones is determined, and the game proceeds to the win/loss determination
- If the win/loss determination result does not line up 5 black or white stones, the game continues by returning to the original stone probability.
- If the game continues, the stones on the board return to the state before the "observation" and are marked with probabilities, which do not affect future observations → There is no guarantee that black will be black in the next observation even if it is black in the n-th observation
- If 5 black or white stones are lined up at the time of the win/loss determination, the side with 5 stones lined up wins and the game ends
- If both black and white stones are lined up by the "observation", the side that made the "observation" wins
- If the board is full and there is no winner, the game is a draw

## How to run
You can run the html file by double-clicking on it.
If you want to reset the game, press the F5 key.

## Program description
[Gomoku.html](/Gomoku.html) is a normal Gomoku game.
[quantaization_gomoku_vs_CPU_select_turn.html](/quantaization_gomoku_vs_CPU_select_turn.html) is a quantum Gomoku game. The opponent is the CPU. You can choose the first or second move.
[quantaization_gomoku_two_people.html](/quantaization_gomoku_two_people.html) is a quantum Gomoku game. The opponent is a player. It is created for simulation with 2 people or 1 person.




