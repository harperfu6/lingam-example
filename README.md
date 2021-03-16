BMLiNGAMを使った因果探索

- docs: https://taku-y.github.io/bmlingam/index.html
- web page: https://note.com/dd_techblog/n/n4255b7ac93ed
- github: https://github.com/cdt15/bmlingam


requirements
check libraly version!!
- python=3.7.3
- scipy=1.2.1
- pymc3=3.10.0
- arviz=0.11.0
- theano

fix libraly
```
# コマンドライン実行のコード修正
!sed -i -e '278 s/df.as_matrix()/df.values/g' /path/to/python/dist-packages/bmlingam/commands/bmlingam_causality.py

# BMLiNGAMの因果係数推定のコード修正
!sed -i -e '11 s/estimate_coeff_posterior/bmlingam_coeff/g' /path/to/bmlingam-coeff
!sed -i -e '412 s/Model(verbose=verbose)/Model()/g' /path/to/python/dist-packages/bmlingam/bmlingam_pm3.py
```
