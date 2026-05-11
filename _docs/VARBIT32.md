# VARBIT32

The varbit32 encodes integers up to 32-bits into a length-prefixed bitstream.

- <span style="color: rgb(22, 145, 121);">Confirmed (can be swapped with Varint16, notably in the item level)</span>
- Major type is: `110`
- Is followed by <span style="text-decoration: underline;">exactly one</span> block of 5-bits.
    - =&gt; length of the payload ahead. (LSB-first)
- Is followed by a variable amount of bits =&gt; payload.
    - Payload is ordered LSB-first.

```
Type   Length   Data
vvv    vvvvv    vvv
110    11000    101
                ^^^
           =bin:101
           =int:5
```@UAt1%SjH49B!JKCp-7#<DD8(?aVDQGlnVcAWF!*Eqz%mRz2!;n~fq8BP9u-_ru5$%b*ee~uQ2q+H%GWSdy@I*i6;I%=e5-Q>YuGAX!Cd/dh6=_CrV8c?mI~I2*NWCk*Gjg^<S<nwg0UPG3E;2)1y/)~m?}QOUhWFF@K>}~yjQYUx>vSUv{k%SvQ@fPwpAg5u`Cq`;IH=uU-&DUE1oNvE1fHwDjF&tDj6yrDjO>rD;_HuD;+BvE59nd!CCeSk8oGNg0&14DPXQg1yXn`5TR4~UFHg}uvUA5qx==ml}=!+dj&(dEBC=t(NghJ$ax`W3*;0lI<gisEg0Vam2vDf#sQ9SlsPw4ps%WZss${Bks%)#stJtf=tJJH^ul%d?1#j3YeZgJ+3bZg*rGlj#70KYLLWN=&DiXn8_6omnR{w&d^1aLzZ(yx=1xxrVe=2;zUG@sEa8`eUukyFd6+d9E_XSt@D_<&H!CdwVr*Kw3f~Uf#qNn1glBd$8LbXDzLcKzxLZyrq&0wl$1!H(B7@=Q=3cRpZ<ASF=71&U(;HXfnP^wU_P^iNNdRQva!CIaQlqgnlf}^Yz?BJ_!1#1*55-S!f5i1od6Dyd(RMrZ{a8x&fzX}yx72Fj(6}%OE72Xxy72g%ymEM(p6@3+d6?~O`mDpga%LQgQDl@@eg$n-){)+#K{!0H!&kD/p&x+1U&r0qvRds^1oE075uVRH)7%Mu#QO*kX@Kv!wsUoRjsS>GDsWP#Q6%Amo#/2(^D{!Gu#tQtfRpWxUJQX-lt78RgSSne;T;2+%C{/&DqbwEZ;HyssY7{GcD/#z_D/st@D_Fr&)(YluRX2jMiWTf&t7`>oI4WDgT*V69FjVD&yBrl+;H<)hRv0TX!BLJ1^zc=oLZNcMj1_%gt>*<#cq{uV_`zG&3Z8IRcY>uNrDCNLrBbCbqaveXqY/T1qcXp8uS^xYV5!#ycK9lvD;&X4_6q%QRqukga;Hoc+hD5K1!njv_bYV4Q??52a8+-Dql^{pV5?^ZYj`SHp;Lwm?66g1g0nmo7*MUqt=O%^t<<f/sobv91y<NAHNjE73apB)imXblO03G%iq(qLO4Ul#%Jho$iu6kLO7zOj%8f8rt%9vw6/3N?T&z<CLf9+$!B^f2%!<v5%u3Bl%*uz#{V-MSg11~1JK(KcsZ#}V*eaF5SiTChinWTgO0`O~%I(UnFjj4Xqg)m1;H+GzQw4umD*3@%-U`0T-Y``4g1ej*UEr@=t5XGP*eX@QT)qm8%Jnc+t%9{&6)WJY(67*_aIA2uaH+_t*r~*+)Tzv?T&+_DO4uuv!BoBq<;tZnRxN^/TowJ`tk9~^uF$E_t<b97ECpM;z^ip/6>hfzt<~UFyJ1%9a4Oxt1zWSgt9K+7ZopN#JPNm8fmZ4TTdEaq#saP1;8nVk3b#xu-7W=Nr68+!I2CTz0<G4-Rk{)iw_<@-=wK?{yaijgK&y0U6>jwct<%6&x/9mHT7g#Ug<G$Ht9ED=ZteoD+Mrdt^a{6H!B*)/D&1NITeuZ&$W^+S3b%HFR_;(L-O#IaC>3sp0<GV`RlC><w?_e1>Ch_OoCRzpAgzR?6/j_owi1w5!cq#@N<mu*NGf4~sfGfk7z&tRDq(=Bh61J-3YcIjVSuTI0;U)Wm/!YlfT@N8rWgvCU@BpNsfGfk7z)X7D<#0Jmjbd}3dwLQCBUqg0<v5R$#5$rz^s=7vRn$ua4RLitd/0^Tnfo>D<#0Ic5oGL&H}C3z*W0A3b$tgR_x#^-JAtmvw*91a20OO0<GD=Rl7I}w`T!X?BFWhoCRC6fU9<J6>iP~t=Yg;x^xP+PJveG&??<J1zV>;t90lUZk+<H)1XzlbPBglfmZ3zD&0B-Tc<#)bm$dsodT`XpjEnb3b#&yR_V/x-5dp5qkyY)a20Nj0<F=&Rk}C/w?_e1=-?{d90gmWfU9(H6>g3Kt<k_$x;P5AM*&vo;40l51zV$lt8{P`ZuSDL-oRD6*b29M0aou/D&6b_TfKm*cd!+1_5c/# Byte-compiled.git status

