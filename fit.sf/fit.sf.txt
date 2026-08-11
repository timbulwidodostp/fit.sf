# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Non-parametric stochastic frontier Use fit.sf (snfa) With (In) R Software
install.packages("snfa")

library("snfa")
# Estimation Non-parametric stochastic frontier Use fit.sf (snfa) With (In) R Software
fit.sf = read.csv("https://raw.githubusercontent.com/timbulwidodostp/fit.sf/main/fit.sf/fit.sf.csv",sep = ";")
fit.sf <- fit.sf[complete.cases(fit.sf),]
X <- as.matrix(fit.sf[,c("K", "L")])
y <- fit.sf$Y
fit.sf <- fit.sf(X, y, X.constrained = X, method = "mc")
head(fit.sf$y.fit, 2)
head(fit.sf$gradient.fit, 2)
fit.sf$mean.efficiency
head(fit.sf$mode.efficiency, 2)
head(fit.sf$X.eval, 3)
head(fit.sf$X.constrained, 2)
head(fit.sf$X.fit, 2)
fit.sf$H.inv
fit.sf$method
fit.sf$scaling.factor
# Non-parametric stochastic frontier Use fit.sf (snfa) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished