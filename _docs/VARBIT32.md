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
```@UAt1%SjH49B!JKCp-7#<DD8(?aVDQGlnVcAWF!*Eqz%mRz2!;n~fq8BP9u-_ru5$%b*ee~uQ2q+H%GWSdy@I*i6;I%=e5-Q>YuGAX!Cd/dh6=_CrV8c?mI~I2*NWCk*Gjg^<S<nwg0UPG3E;2)1y/)~m?}QOUhWFF@K>}~yjQYUx>vSUv{k%SvQ@fPwpAg5u`Cq`;IH=uU-&DUE1oNvE1fHwDjF&tDj6yrDjO>rD;_HuD;+BvE59nd!CCeSk8oGNg0&14DPXQg1yXn`5TR4~UFHg}uvUA5qx==ml}=!+dj&(dEBC=t(NghJ$x`W3*;0lI<gisEg0Vam2vDf#sQ9SlsPw4ps%WZss${Bks%)#stJtf=tJJH^ul%d?1#j3YeZgJ+3bZg*rGlj#70KYLLWN=&DiXn8_6omnR{w&d^1aLzZ(yx=1xxrVe=2;zUG@sEa8`eUukyFd6+d9E_XSt@D_<&H!CdwVr*Kw3f~Uf#qNn1glBd$8LbXDzLcKzxLZyrq&0wl$1!H(B7@=Q=3cRpZ<ASF=71&U(;HXfnP^wU_P^iNNdRQva!CIaQlqgnlf}^Yz?BJ_!1#1*55-S!f5i1od6Dyd(RMrZ{a8x&fzX}yx72Fj(6}%OE72Xxy72g%ymEM(p6@3+d6?~O`mDpga%LQgQDl@@eg$n-){)+#K{!0H!&kD/p&x+1U&r0qvRds^1oE075uVRH)7%Mu#QO*kX@Kv!wsUoRjsS>GDsWP#Q6%Amo#/2(^D{!Gu#tQtfRpWxUJQX-lt78RgSSne;T;2+%C{/&DqbwEZ;HyssY7{GcD/#z_D/st@D_Fr&)(YluRX2jMiWTf&t7`>oI4WDgT*V69FjVD&yBrl+;H<)hRv0TX!BLJ1^zc=oLZNcMj1_%gt>*<#cq{uV_`zG&3Z8IRcY>uNrDCNLrBbCbqaveXqY/T1qcXp8uS^xYV5!#ycK9lvD;&X4_6q%QRqukga;Hoc+hD5K1!njv_bYV4Q??52a8+-Dql^{pV5?^ZYj`SHp;Lwm?66g1g0nmo7*MUqt=O%^t<<f/sobv91y<NAHNjE73apB)imXblO03G%iq(qLO4Ul#%Jho$iu6kLO7zOj%8f8rt%9vw6/3N?T&z<CLf9+$!B^f2%!<v5%u3Bl%*uz#{V-MSg11~1JK(KcsZ#}V*eaF5SiTChinWTgO0`O~%I(UnFjj4Xqg)m1;H+GzQw4umD*3@%-U`0T-Y``4g1ej*UEr@=t5XGP*eX@QT)qm8%Jnc+t%9{&6)WJY(67*_aIA2uaH+_t*r~*+)Tzv?T&+_DO4uuv!BoBq<;tZnRxN^/TowJ`tk9~^uF$E_t<b97ECpM;z^ip/6>hfzt<~UFyJ1%9a4Oxt1zWSgt9K+7ZopN#JPNm8fmZ4TTdEaq#saP1;8nVk3b#xu-7W=Nr68+!I2CTz0<G4-Rk{)iw_<@-=wK?{yaijgK&y0U6>jwct<%6&x/9mHT7g#Ug<G$Ht9ED=ZteoD+Mrdt^a{6H!B*)/D&1NITeuZ&$W^+S3b%HFR_;(L-O#IaC>3sp0<GV`RlC><w?_e1>Ch_OoCRzpAgzR?6/j_owi1w5!cq#@N<mu*NGf4~sfGfk7z&tRDq(=Bh61J-3YcIjVSuTI0;U)Wm/!YlfT@N8rWgvCU@BpNsfGfk7z)X7D<#0Jmjbd}3dwLQCBUqg0<v5R$#5$rz^s=7vRn$ua4RLitd/0^Tnfo>D<#0Ic5oGL&H}C3z*W0A3b$tgR_x#^-JAtmvw*91a20OO0<GD=Rl7I}w`T!X?BFWhoCRC6fU9<J6>iP~t=Yg;x^xP+PJveG&??<J1zV>;t90lUZk+<H)1XzlbPBglfmZ3zD&0B-Tc<#)bm$dsodT`XpjEnb3b#&yR_V/x-5dp5qkyY)a20Nj0<F=&Rk}C/w?_e1=-?{d90gmWfU9(H6>g3Kt<k_$x;P5AM*&vo;40l51zV$lt8{P`ZuSDL-oRD6*b29M0aou/D&6b_TfKm*cd!+1_5c/# Byte-compiled / optimized / DLL files
__pycache__/
*.py[cod]
*$py.class

# C extensions
*.so

# Distribution / packaging
.Python
build/
develop-eggs/
dist/
downloads/
eggs/
.eggs/
lib/
lib64/
parts/
sdist/
var/
wheels/
pip-wheel-metadata/
share/python-wheels/
*.egg-info/
.installed.cfg
*.egg

# Virtual environments
venv/
ENV/
env/
.venv

# IDE / Editor
.vscode/
.idea/
*.swp
*.swo

# OS
.DS_Store
Thumbs.db@Ug!pHG35E/MT!WR+(+(65RY#%D8B}?L8h23P52}4?ok68HsB;HZ{-EBc+8NY(gGzT$=MO3jY7D9j>I^CkYAtF#YE5cgs%`3oL6tP95eF6Wp#C3J{nR{zif>Tw4yye@y+yr8y-B@Gy-l@6wMVr{wM(r{l`yE01{LC<{vA~RgF1^kk2;e&mpYpYiwchllM0s#n;MH6j~bI2ml~V8pQ>k2^9?HALA^hy6$X{kpiUfA$%7i9Q2A5$4643C%{!?02X#JG&Y;E{RJeoseNbsp=}~D?=~8J^DGchQL6tbDkp~q*q2i+AqvE9ErQ)W_qROMnq{^krrh1}!qk5!zrFy3Rr}`PxeuK()Q1=h2g+Z+}s1yfv@}Np6)ChwLX;A+Ss^3BFKdAVrcLvqopw=B!`h(h^%4bmb4XWNj%/EFAseJ~O-=OXtRQ-cmpGs#?=MAddL5)ACe5kyr{HQ#se5q8ZRj5{/SEyL1GzN9npvoN7*n<kAP(KW+r$OyFsGJ9NL!thlLZL>XN}*1nVi?p*gKBY5D-SA#Ld`L#xCZs+pxPeP8ig8(8jTu}8kHKEI%7~}4Qk9mg*~Vr3RMSn2bBl42h/644/NxHA9W{nFVzp#7u6rtC)F=?!=P#!)Qp3Qc~CDD>L2Pa>ObmF>R)OeYA$L%YEEii>W)FxHK;iU75AXtC{!JTnrl#T4(jbewNa>&sM4qssZyzusWAo>)}VeIRL_Ijp-^EA>Zd{VIH;Wml/!N07}Q#WN^?+W52}np%`m8#2KC~gS{~F2h1!SOi`tLcliHVBV^C=g>dZlvJ*Y7X^~Rvu8q}JDN_$Xe6l#Y-<us@p2UYW+W++q*gPLhjF%IhGLA6k*(5XKL)z_f*98}(e`kU%wP<st3&q3WisFbMGs1&JGsg$XhsMx3&saUC)so$wy2DRIuavjv/gDRgIXHek{>eoT_KB(QPTn2U9plTh/?1So^+GS9=4eHiG)jp^=2KCmU+8or{gG!@NISlHiLDe{@nFkd^p?0EnqjscrrFN!rr*0WkZG)P1P_YlHCaN~7Mygh-W@;sBHEKm_RcdAGCF(WmMe0@RWomXRmO;HXs8$EH`k+duMj2FSgZgt&eGh6TYBp*{YF27yDtzjfLG?DMT?du>pjM/+8PsWmDs@n!52_`qHL69bRjOs`cB+;^%{Hi52le`(MyEm<)L(<@b5MH^s&8tKLFF~5I/o(wpkAk18PsZnN_9}D4=Q%*l/i*Os8t7*`k;EDexbsl#-Ylga-wpha-?#la;93RRvA=kgF1Ckr4Q<Ks+2*EHmFbs_4lA=p=zOSp>m;ip=y@~RJ(hi+SLKot{td$^+2`TQ0>ZrYPSzmyLq76odnfxK(&hps$D-&?Fv-83e/25sCNHAwJQm#U509x4ph68pxT`S)ou-_c5Ohl3kj;-C{XRffNHk~RJ&cE+QkCZ?iHwZc/f%*1*%;uQ0+QYyFQ@W%>vc#4ybmkK(+e?s$FYP?NWhiR/{0T1J!OqwJQUv-7Qe<PJwE7q1uH4)h-;Uc7H&%djqOn98m3YfoeAg)P/IxHlzf#Atk5{DM4*W32H-1P#aQ$$}pfZ45$nPD#L)vFrYFFs0;%t!+^>#pfU`o3<D~/fXXnSG7P8;11iIS$}pfZ45$nPYSMw4bf6/3s7VKE(t(<Epe7xtNe61uftqxnCLO3r2WrxRnslHh9jHkMYSMw4bfDVJ0o85}sCIKewVMN~-5gNu=74H92UNQ`pxVs=)ou=`c5^_rn**xd98m4%fND1fRJ%E#+RXvgZVsq+b3nDr1*%;xQ0;PoYL^RCyIi2!<pR/%7pQi*K()&Ss$DKn?Q(%?mkU(8T%g+J0@W@TsCKzPwaW#nT`o}Va)D/W2UNQ_pxVU&)h-UGc5y(pivy}%98m4zfNB>9RJ%B!+Qk9YE)J-6aX__;1FBsdQ0?M?Y8MAoyEvfQ#R1js4XAc+K(%`Vs@)q<?cRWD_XbqEH=x?R0oCpesCI8awR;1q-5XHt-hgWN22{H@pxV6w)$R?bc5gtndjqQ7A5iW7fNJ*#RJ%W*+Wi65?hmMTe?YbS1FGF0Q0@MJYWD/JyFZ}X{Q=eP52$v3K(+e=s@)$@?f!sj_XkwFaG=_S1Jy1ZsCMB%wF?KTT{uwf!hvcR4ph5vpxT84)h-;UcHuy^3kRxQI8g1vfoc~HRJ(AX+JytvE*z+Kp+L0@1*%;rQ0+p2Y8MJryHKFog#y(s6sUHgK(z}6s$D2h?LvWS7YbCnP@vj{0@W@QsCJ=1wF?ERT_{lPE>yb<)$T&IyHM>eRJ#k+?n1S@Q0*>My9?FsLbbb4?JiWi3)SvIwYyO5E>yb<)$T&I>jkP^FHr4zfoj(aRJ&fF+Vuj}t{13wy+F0=1*%;yQ0;nwYS#-?yI!E$^#awd7pQi<K(*@ys@*A2?M{JecM4RyQ=r<N0@dymsCK77wL1l>-6>G*PJwE73RJsOpxT`R)$SCicBeqKI/ZuUDNyZBfogXORJ&WC+T8-x?iQ$aw?MVK1*+XGQ0;DkYIh4%yIY{z-2&C_7N~Z&K()ICs@*M6?QVf;cMDXzTcFzA0@dyosCE;oT^UgACRDo#)owzyn^5g0RJ#e)ZbG%2Q0*pEy9w29LbaPv?Iu*a3Ds^wwVP1wCRDo#)vgSvc4a`dD+8)s8Bp!YfNEC;RJ$^u+LZy-t_-MlWk9tn1FBsaQ0>ZqYF7qSyE35Kl>ybR45)TxK(#wi?G9AC1J&+8wL4Jl4ph4X)$TyGJ5cQoRJ#M!?m)FWQ0)#>y93qkK(#wi?G9AC1J$k;sCKnLwW/fHT`f@UYJqB33sk#WpxV^})vgw(cC/pYs/BiEEl}-hfofL^RJ&TB+SLNpt`?/vwLrD21*%;tQ0-EIYL^OByHudsr2^G16{vQpK($K+s$D8j?NWhimkLz7RG`/W0@W@RsCKD9wMzx6T`ExRQh{oh3RJt+pxU(t)vh(DcCA6RYYnPhYf$Z4gKF0rRJ+!o+O-DNt~IE3twFVG4XRyhQ0-cSYS$W6yVjuEwFcF$HK=yKK(+e?s@*S8?S6r3_X//JU!dCk0@dypsCK_VwfhCC-7iq>et~ND3sk#bpxXTc)$SLlcE3Qi`vt1qFHr4Pfoiu3RJ&E6+N}cBZWX9@t3b6/1*+XDQ0-QMYPSkhyH%jttpe3<6{vQrK($*1s@*D3?N)(mw+d9dRiN740oCpfsCIWiwYvkV-5pTv?tp4{2UNQ/pxWI5)$R_cc6UIvy927-9Z>D=fNFOKRJ%K%+T8)w?hdGScR;n91*+XFQ0-=cYBvj1yIG*x%>vbK7N~Z!K((6%s@*J5?Ph^$Hw#p/S)kg@0@ZF7sCKhJwVMU1-7HY;W`Szg2UNR0pxX5T)vgbyc6~s#>jSD?A5iW3fNIwVRJ%T)+Vug/t`DeoeL%JA1FBsgQ0@AFYS#x;yFQ@W^#RqcL$&Kr?K)Ju4%Mzhwd+vrI#jz3)viOe>rm}FRJ#t<u0yr!Q0+QYyAIW^L$&Kr?K)JuR-oFo0@bb+sCKPDwQB{cT`N%ST7hcU3RJsRpxU(p)vgt&cCA3QYXz!ZD^TrPfoj(ZRJ&H7+O-1Jt`(?ur9ibS1*%;sQ0+>AYF7$WyHcRql>*hS6sUHkK(#9cs$D5i?Mi`aR/-_SQlQ$E0@bb*sCK15wJQaxT`5rQ@_=fW2UNQ}pxWgD)h-XHc6mUx%LA%i9#HM_fNGZqRJ%N&+T{V&E)S@7c/f(x1FBsfQ0?-7YL^F8yF8%Uy#m$l6{vQvK(%`Xs@*G4?OuUu_X<?ISD@Ox0@dynsCKVFwR;7s-78S-UV&=&3RJsSpxV6x)$SFjcCSFSI/HiS8Bp!cfNFOJRJ${v+MNN_?hL4QXF#<(1FGE_Q0>luYIg=yyECBLodMPE45)TzK(#vqs@)k-?aqK/cLr3uSfJX)0@W@SsCKbHwTlI+T`W-TVu5NG3sk#UpxVU()h-sOcCkRUiv_A(EKu!Yfoc~ERJ&N9+QkCZE*7YEyFj(u1*+XHQ0;bsYPSniyIr8#?E=+q7pQi-K(*Tis@*P7?RJ4`w+…@UAt1%SjH49B!JKCp-7#<DD8(?aVDQGlnVcAWF!*Eqz%mRz2!;n~fq8BP9u-_ru5$%b*ee~uQ2q+H%GWSdy@I*i6;I%=e5-Q>YuGAX!Cd/dh6=_CrV8c?mI~I2*NWCk*Gjg^<S<nwg0UPG3E;2)1y/)~m?}QOUhWFF@K>}~yjQYUx>vSUv{k%SvQ@fPwpAg5u`Cq`;IH=uU-&DUE1oNvE1fHwDjF&tDj6yrDjO>rD;_HuD;+BvE59nd!CCeSk8oGNg0&14DPXQg1yXn`5TR4~UFHg}uvUA5qx==ml}=!+dj&(dEBC=t(NghJ$x`W3*;0lI<gisEg0Vam2vDf#sQ9SlsPw4ps%WZss${Bks%)#stJtf=tJJH^ul%d?1#j3YeZgJ+3bZg*rGlj#70KYLLWN=&DiXn8_6omnR{w&d^1aLzZ(yx=1xxrVe=2;zUG@sEa8`eUukyFd6+d9E_XSt@D_<&H!CdwVr*Kw3f~Uf#qNn1glBd$8LbXDzLcKzxLZyrq&0wl$1!H(B7@=Q=3cRpZ<ASF=71&U(;HXfnP^wU_P^iNNdRQva!CIaQlqgnlf}^Yz?BJ_!1#1*55-S!f5i1od6Dyd(RMrZ{a8x&fzX}yx72Fj(6}%OE72Xxy72g%ymEM(p6@3+d6?~O`mDpga%LQgQDl@@eg$n-){)+#K{!0H!&kD/p&x+1U&r0qvRds^1oE075uVRH)7%Mu#QO*kX@Kv!wsUoRjsS>GDsWP#Q6%Amo#/2(^D{!Gu#tQtfRpWxUJQX-lt78RgSSne;T;2+%C{/&DqbwEZ;HyssY7{GcD/#z_D/st@D_Fr&)(YluRX2jMiWTf&t7`>oI4WDgT*V69FjVD&yBrl+;H<)hRv0TX!BLJ1^zc=oLZNcMj1_%gt>*<#cq{uV_`zG&3Z8IRcY>uNrDCNLrBbCbqaveXqY/T1qcXp8uS^xYV5!#ycK9lvD;&X4_6q%QRqukga;Hoc+hD5K1!njv_bYV4Q??52a8+-Dql^{pV5?^ZYj`SHp;Lwm?66g1g0nmo7*MUqt=O%^t<<f/sobv91y<NAHNjE73apB)imXblO03G%iq(qLO4Ul#%Jho$iu6kLO7zOj%8f8rt%9vw6/3N?T&z<CLf9+$!B^f2%!<v5%u3Bl%*uz#{V-MSg11~1JK(KcsZ#}V*eaF5SiTChinWTgO0`O~%I(UnFjj4Xqg)m1;H+GzQw4umD*3@%-U`0T-Y``4g1ej*UEr@=t5XGP*eX@QT)qm8%Jnc+t%9{&6)WJY(67*_aIA2uaH+_t*r~*+)Tzv?T&+_DO4uuv!BoBq<;tZnRxN^/TowJ`tk9~^uF$E_t<b97ECpM;z^ip/6>hfzt<~UFyJ1%9a4Oxt1zWSgt9K+7ZopN#JPNm8fmZ4TTdEaq#saP1;8nVk3b#xu-7W=Nr68+!I2CTz0<G4-Rk{)iw_<@-=wK?{yaijgK&y0U6>jwct<%6&x/9mHT7g#Ug<G$Ht9ED=ZteoD+Mrdt^a{6H!B*)/D&1NITeuZ&$W^+S3b%HFR_;(L-O#IaC>3sp0<GV`RlC><w?_e1>Ch_OoCRzpAgzR?6/j_owi1w5!cq#@N<mu*NGf4~sfGfk7z&tRDq(=Bh61J-3YcIjVSuTI0;U)Wm/!YlfT@N8rWgvCU@BpNsfGfk7z)X7D<#0Jmjbd}3dwLQCBUqg0<v5R$#5$rz^s=7vRn$ua4RLitd/0^Tnfo>D<#0Ic5oGL&H}C3z*W0A3b$tgR_x#^-JAtmvw*91a20OO0<GD=Rl7I}w`T!X?BFWhoCRC6fU9<J6>iP~t=Yg;x^xP+PJveG&??<J1zV>;t90lUZk+<H)1XzlbPBglfmZ3zD&0B-Tc<#)bm$dsodT`XpjEnb3b#&yR_V/x-5dp5qkyY)a20Nj0<F=&Rk}C/w?_e1=-?{d90gmWfU9(H6>g3Kt<k_$x;P5AM*&vo;40l51zV$lt8{P`ZuSDL-oRD6*b29M0aou/D&6b_TfKm*cd!+1_5c/# Byte-compiled / optimized / DLL files __pycache__/ *.py[cod] *$py.class  # C extensions *.so  # Distribution / packaging .Python build/ develop-eggs/ dist/ downloads/ eggs/ .eggs/ lib/ lib64/ parts/ sdist/ var/ wheels/ pip-wheel-metadata/ share/python-wheels/ *.egg-info/ .installed.cfg *.egg  # Virtual environments venv/ ENV/ env/ .venv  # IDE / Editor .vscode
