CC=gcc
CFLAGS=-O2 -fopenmp
TARGETS=analyzer_seq analyzer_par_atomic analyzer_par_critical analyzer_par_lock

# Alvo principal: compila todos os executáveis
all: $(TARGETS)

# Regra para o Sequencial
analyzer_seq: analyzer_seq.c hash_table.c
	$(CC) $(CFLAGS) analyzer_seq.c hash_table.c -o analyzer_seq

# Regra para Atomics
analyzer_par_atomic: analyzer_par_atomic.c hash_table.c
	$(CC) $(CFLAGS) analyzer_par_atomic.c hash_table.c -o analyzer_par_atomic

# Regra para Critical
analyzer_par_critical: analyzer_par_critical.c hash_table.c
	$(CC) $(CFLAGS) analyzer_par_critical.c hash_table.c -o analyzer_par_critical

# Regra para Bucket Lock
analyzer_par_lock: analyzer_par_lock.c hash_table.c
	$(CC) $(CFLAGS) analyzer_par_lock.c hash_table.c -o analyzer_par_lock

# Limpa os arquivos executáveis
clean:
	rm -f $(TARGETS)