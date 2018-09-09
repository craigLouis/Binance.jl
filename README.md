# Binance.jl
[Binance](https://www.binance.com/en?ref=35360148) API with [Julialang](https://julialang.org/)

![julia](https://julialang.org/v2/img/logo.svg)

![binance](data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI2MzIuMDE0IiBoZWlnaHQ9IjEyNi42MTEiPjxwYXRoIGZpbGw9IiNmNWJjMDAiIGQ9Ik0zOC4xNzEgNTMuMjAzbDI0LjU4OC0yNC41ODcgMjQuNjAxIDI0LjYgMTQuMzA3LTE0LjMwN0w2Mi43NTkgMCAyMy44NjQgMzguODk2ek0xMy43NiA0OC45OTdsMTQuMzA3IDE0LjMwNkwxMy43NiA3Ny42MTEtLjU0NyA2My4zMDR6bTI0LjQxMSAyNC40MTFsMjQuNTg4IDI0LjU4NyAyNC42LTI0LjU5OSAxNC4zMTUgMTQuMjk5LS4wMDcuMDA4LTM4LjkwOCAzOC45MDgtMzguODk2LTM4Ljg5NS0uMDItLjAyem04Ny44OTUtMTAuMDk4TDExMS43NiA3Ny42MTcgOTcuNDUyIDYzLjMxMWwxNC4zMDctMTQuMzA4eiIvPjxwYXRoIGZpbGw9IiNmNWJjMDAiIGQ9Ik03Ny4yNzEgNjMuMjk4aC4wMDZMNjIuNzU5IDQ4Ljc4IDUyLjAzIDU5LjUwOWgtLjAwMWwtMS4yMzIgMS4yMzMtMi41NDMgMi41NDMtLjAyLjAyLjAyLjAyMSAxNC41MDUgMTQuNTA1IDE0LjUxOC0xNC41MTguMDA3LS4wMDh6bTcxLjA5OS0zMi42MTloMzEuMTE3YzcuNzIzIDAgMTMuNTYzIDEuOTgyIDE3LjUyMSA1Ljk0NiAzLjA2MyAzLjA3IDQuNTk0IDYuODc1IDQuNTk0IDExLjQxNHYuMTkyYzAgMS45MTgtLjIzNyAzLjYxMy0uNzE0IDUuMDgzYTE1LjgwNyAxNS44MDcgMCAwIDEtMS45MDcgMy45OCAxNS4xNjMgMTUuMTYzIDAgMCAxLTIuNzYzIDMuMTE3IDE4LjUyNiAxOC41MjYgMCAwIDEtMy4zODMgMi4zMDJjMy44ODIgMS40NzIgNi45MzggMy40NjkgOS4xNjYgNS45OTUgMi4yMjcgMi41MjcgMy4zNDIgNi4wMjggMy4zNDIgMTAuNTAzdi4xOTFjMCAzLjA3LS41OSA1Ljc1NS0xLjc3MSA4LjA1OC0xLjE4MSAyLjMwMS0yLjg3MyA0LjIyLTUuMDc2IDUuNzU1LTIuMjAzIDEuNTM1LTQuODUyIDIuNjg1LTcuOTQ4IDMuNDUzLTMuMDk2Ljc2Ny02LjUyNyAxLjE1LTEwLjI5MiAxLjE1SDE0OC4zN1YzMC42Nzl6bTI4LjAwNiAyNy4xNDNjMy4yNjIgMCA1Ljg1Mi0uNTU4IDcuNzY5LTEuNjc4IDEuOTE4LTEuMTE5IDIuODc3LTIuOTI2IDIuODc3LTUuNDE5di0uMTkyYzAtMi4yMzctLjgzMi0zLjk0Ny0yLjQ5NC01LjEzMS0xLjY2My0xLjE4My00LjA2MS0xLjc3NS03LjE5My0xLjc3NWgtMTQuNTc5djE0LjE5NWgxMy42MnptMy45MzMgMjcuMDQ5YzMuMjYxIDAgNS44MTctLjU5IDcuNjczLTEuNzc0IDEuODU0LTEuMTgzIDIuNzgyLTMuMDIyIDIuNzgyLTUuNTE2di0uMTkxYzAtMi4yMzgtLjg2NC00LjAxMi0yLjU5LTUuMzI0LTEuNzI3LTEuMzA5LTQuNTA4LTEuOTY1LTguMzQ1LTEuOTY1aC0xNy4wNzN2MTQuNzcxaDE3LjU1M3ptNDMuNTY2LTU0LjE5MmgxNC43NzJWOTcuODJoLTE0Ljc3MlYzMC42Nzl6bTM3LjE0NSAwaDEzLjYxOGwzMS40NjEgNDEuMzR2LTQxLjM0aDE0LjU3OVY5Ny44MmgtMTIuNTY0bC0zMi41MTYtNDIuNjgyVjk3LjgySDI2MS4wMlYzMC42Nzl6bTEwNC4zNzgtLjQ3OWgxMy42MTlsMjguNzc2IDY3LjYySDM5Mi4zNWwtNi4xMzktMTUuMDU4SDM1Ny44MmwtNi4xMzggMTUuMDU4aC0xNS4wNjFsMjguNzc3LTY3LjYyem0xNS41MzggMzkuNTE2bC04LjkyMS0yMS43NzItOC45MTggMjEuNzcyaDE3LjgzOXptNDIuODAyLTM5LjAzN2gxMy42MjFsMzEuNDU5IDQxLjM0di00MS4zNGgxNC41NzlWOTcuODJoLTEyLjU2NGwtMzIuNTE2LTQyLjY4MlY5Ny44MmgtMTQuNTc5VjMwLjY3OXpNNTM2LjU1NyA5OC45N2MtNC45MjYgMC05LjQ5Ni0uODk2LTEzLjcxNy0yLjY4NXMtNy44NjUtNC4yMzYtMTAuOTM0LTcuMzM4Yy0zLjA3LTMuMTAxLTUuNDY5LTYuNzYyLTcuMTkzLTEwLjk4Mi0xLjcyNy00LjIyMS0yLjU5LTguNzI5LTIuNTktMTMuNTI1di0uMTkxYzAtNC43OTYuODYzLTkuMjg3IDIuNTktMTMuNDc2IDEuNzI1LTQuMTg4IDQuMTIzLTcuODY1IDcuMTkzLTExLjAzIDMuMDY4LTMuMTY1IDYuNzQ2LTUuNjYgMTEuMDI5LTcuNDgyczkuMDE4LTIuNzMzIDE0LjE5Ny0yLjczM2MzLjEzMSAwIDUuOTkyLjI1NyA4LjU4Mi43NjcgMi41OS41MTMgNC45MzkgMS4yMTUgNy4wNTEgMi4xMWEzMC43MTQgMzAuNzE0IDAgMCAxIDUuODUyIDMuMjYxIDM5Ljg2NSAzOS44NjUgMCAwIDEgNC45ODYgNC4yMjFsLTkuMzk4IDEwLjgzOGMtMi42MjUtMi4zNjUtNS4yOTMtNC4yMjEtOC4wMS01LjU2My0yLjcxOS0xLjM0Mi01Ljc3MS0yLjAxNC05LjE2LTIuMDE0LTIuODE0IDAtNS40Mi41NDQtNy44MTYgMS42MzFhMTguNTEyIDE4LjUxMiAwIDAgMC02LjE4OCA0LjUwN2MtMS43MjUgMS45MTgtMy4wNjggNC4xNDEtNC4wMjkgNi42NjYtLjk1NyAyLjUyNy0xLjQzNiA1LjIyOC0xLjQzNiA4LjEwNXYuMTkxYzAgMi44NzcuNDc5IDUuNTk2IDEuNDM2IDguMTUyLjk2MSAyLjU1OSAyLjI4NSA0Ljc5NiAzLjk4MiA2LjcxNCAxLjY5MyAxLjkxOCAzLjc0IDMuNDM4IDYuMTM3IDQuNTU3IDIuNCAxLjEyIDUuMDM3IDEuNjc4IDcuOTE0IDEuNjc4IDMuODM4IDAgNy4wOC0uNzAzIDkuNzM0LTIuMTEgMi42NTQtMS40MDUgNS4yOTMtMy4zMjQgNy45MTQtNS43NTVsOS40IDkuNDk2YTQ4LjgxMiA0OC44MTIgMCAwIDEtNS4zNzEgNC45ODcgMzEuOTI0IDMxLjkyNCAwIDAgMS02LjA5MiAzLjc5Yy0yLjIwNSAxLjA1NC00LjYyMSAxLjg1NS03LjI0IDIuMzk3LTIuNjI0LjU0My01LjU2NC44MTYtOC44MjMuODE2em00NC45MS02OC4yOTFoNTAuNTQ3VjQzLjgyaC0zNS45Njd2MTMuNjJoMzEuNjUydjEzLjE0aC0zMS42NTJ2MTQuMWgzNi40NDl2MTMuMTRoLTUxLjAyOVYzMC42Nzl6Ii8+PC9zdmc+)

usage :

```julia
using Pkg;
Pkg.add(PackageSpec(url="https://github.com/DennisRutjes/Binance.jl",rev="master"))

packages=["Dates","DataFrames","Plots","GR"]

for package in packages
    if get(Pkg.installed(),package,-1) == -1
        println(" getting package : ", package)
        Pkg.add(package)
    end
end

# fill in correct values when using private binancecalls e.g. getBalances()
ENV["BINANCE_APIKEY"] = "REDACTED"; 
ENV["BINANCE_SECRET"] = "REDACTED";

using Binance,Dates, DataFrames, Plots

hr24 = Binance.get24HR()
hr24ETHBTC = Binance.get24HR("ETHBTC")

market = Binance.getMarket()
market_BNBBTC = Binance.getMarket("BNBBTC")

function getBinanceKlineDataframe(symbol; startDateTime = nothing, endDateTime = nothing, interval="1m")
    klines = Binance.getKlines(symbol; startDateTime = startDateTime, endDateTime = endDateTime, interval = interval)
    result = hcat(map(z -> map(x -> typeof(x) == String ? parse(Float64, x) : x, z), klines)...)';

    if size(result,2) == 0
        return nothing
    end

    symbolColumnData = map(x -> symbol, collect(1:size(result, 1)));
    df = DataFrame([symbolColumnData, Dates.unix2datetime.(result[:,1]/1000) ,result[:,2],result[:,3],result[:,4],result[:,5],result[:,6],result[:,8],Dates.unix2datetime.(result[:,7] / 1000),result[:,9],result[:,10],result[:,11]], [:symbol,:startDate,:open,:high,:low,:close,:volume,:quoteAVolume, :endDate, :trades, :tbBaseAVolume,:tbQuoteAVolume]);
end

dfKlines = getBinanceKlineDataframe("ETHBTC");

plot(dfKlines[:close])



```
