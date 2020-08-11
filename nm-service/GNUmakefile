
all: dialyzer test

run:
	rebar3 run

dialyzer:
	rebar3 dialyzer

build:
	rebar3 compile

test:
	rebar3 eunit

cover:
	rebar3 eunit --cover
	rebar3 cover

clean:
	$(RM) -r _build

.PHONY: all run dialyzer build test cover clean
