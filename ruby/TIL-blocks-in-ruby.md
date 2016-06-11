## Todo método en Ruby acepta un &block como parámetro

	def mi_metodo
	  puts "Hello, world"
	  yield
	end
	
	mi_metodo do
	  puts "Recibo bloques también, y no le dije a nadie"
	end
	
	