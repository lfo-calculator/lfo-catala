MAIN	=  Title17_MotorAndOtherVehicles
TEST	=  Title17_Test
CATALA	?= catala --language=en
JS	= _build/default/wrapper.bc.js

all: ../frontend/main.js

test: $(TEST).run

%.ml: %.catala_en
	$(CATALA) OCaml $<

%.run: %.catala_en
	$(CATALA) -s $(SCOPE) Interpret -t $<

$(JS): $(MAIN).ml
	dune build --profile=release

../frontend/main.js: $(JS)
	cp $< $@

################################################################################

Title17_Test.run: SCOPE=Penalty286_83_135
