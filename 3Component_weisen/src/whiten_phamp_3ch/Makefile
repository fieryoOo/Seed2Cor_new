INST_DIR = $(HOME)/usr/bin
BIN  = whiten_phamp

fflags = -O2 -Wall -ffixed-line-length-none -m32
cflags = -O2 -Wall -m32

LDLIBS =   -L$(HOME)/usr/lib -lfftw3

FFLAGS = $(DBG) $(fflags)

CFLAGS = $(DBG) $(cflags)

FC = g77

CC = gcc

DBG = -g

FOBJS = driver_c.o whiten_phamp.o swapn.o

$(BIN) : $(FOBJS)
	$(FC) $(FFLAGS) $(CFLAGS) $(FOBJS) -static -o $(BIN) $(LDLIBS) 

install :: $(BIN)
	install -s $(BIN) $(INST_DIR)

clean ::
	rm -f $(BIN) core $(FOBJS)
