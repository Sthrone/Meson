project('DodatneFunkcionalnosti', 'c')
compiler = meson.get_compiler('c')

kod = '''
	
#include <stdio.h>

void Pozdrav()
{
	printf("Pozdrav sa IMI-ja!\n");
}

'''

uspesnost_kompajliranja = compiler.compiles(kod, name : 'Provera kompajliranja')
uspesnost_linkovanja = compiler.links(kod, args : '-lfoo', name : 'Provera linkovanja')

kod = '''

#include <stdio.h>

int main(int argc, char **argv)
{
	printf("%s\n", "Izlaz!");
	fprintf(stderr, "%s\n", "Greska!");
	return 0;
}

'''

rezultat_testiranja = compiler.run(kod, name: 'Testiranje')

if rezultat_testiranja.returncode() == 0
	uspesnost_linkovanja_2 = compiler.links(kod, name : 'Provera linkovanja 2')
endif