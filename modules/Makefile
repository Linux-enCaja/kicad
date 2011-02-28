MODULES= \
	60fbga_ddr \
	66-tsop \
	90vfbga_mobile_ddr \
	DFN10 \
	FGG484bga-p10 \
	header20x2_smd_100mil \
	header25x2_smd_2mm \
	LQFP48 \
	MLF16 \
	MLF20m1 \
	MLP6 \
	MINI-SO-8 \
	SON008V5060 \
	UDFN6 \
	stdpass \
	PVQFN-N20

BUILDID=$(shell date +"%d/%m/%Y-%H:%M:%S")

.SUFFIXES:	.fpd .mod .mdc
.PHONY:		all clean

all:		$(MODULES:%=%.mod) $(MODULES:%=%.mdc)

clean:
		rm -f $(MODULES:%=%.mod)
		rm -f $(MODULES:%=%.mdc)

.fpd.mod:
		fped -k $< $@

.fpd.mdc:
		@echo  PCBNEW-LibDoc----V1 $(BUILDID) > $@
		@echo  $$\EndLIBDOC $(BUILDID) >> $@



