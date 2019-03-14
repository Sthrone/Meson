project('DinamickaBiblioteka', 'c')
pozdrav_lib = shared_library('pozdrav', 'funkcija.c')
exe = executable('program', 'program.c', link_with : pozdrav_lib)
test('Prvi test', exe)