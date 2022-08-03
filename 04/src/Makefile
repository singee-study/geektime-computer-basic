.PHONY: compile
compile:
	iverilog -o wave -y ./  alu_tb.v  alu.v
	vvp -n wave -lxt2

.PHONY: show
show:
	gtkwave wave.vcd

.PHONY: image
image:
	yosys < yosys.do
	dot -Tpng -o alu.png alu.dot

.PHONY: clean
clean:
	rm -f wave wave.vcd alu.dot alu.png
