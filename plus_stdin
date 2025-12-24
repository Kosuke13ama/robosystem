#!/bin/bash -xv
# SPDX-FileCopyrightText: 2025 Kosuke Amano
# SPDX-License-Identifier: BSD-3-Clause

ng () {
	echo ${1}行目が違うよ
	res=1
}

res=0

out=$(seq 5 | python3 plus)
[ "${out}" = 15 ] || ng "$LINENO"

out=$(echo あ | python3 plus)
[ "$?" = 1 ] || ng "$LINENO"
[ "${out}" = "" ] || ng "$LINENO"

out=$(echo | python3 plus)
[ "$?" = 1 ] || ng "$LINENO"
[ "${out}" = "" ] || ng "$LINENO"

[ "${res}" = 0 ] && echo OK
exit $res
