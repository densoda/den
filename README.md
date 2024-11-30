def laminata_izmaksas():
   
    laminata_cena_kvm = float(input("Ievadiet lamināta cenu (€/m2): "))
    pakas_cena = float(input("Ievadiet lamināta pakas cenu (EUR): "))
    pakas_sedzosa_platiba = float(input("Ievadiet lamināta pakas sedzošo platību (m2): "))
    plaksnu_skaits_paka = int(input("Cik plāksnes ir vienā pakā (gab.): "))
    plaksnes_garums = float(input("Ievadiet lamināta plāksnes garumu (m): "))
    plaksnes_platums = float(input("Ievadiet lamināta plāksnes platumu (m): "))
    istabas_garums = float(input("Ievadiet istabas garumu (m): "))
    istabas_platums = float(input("Ievadiet istabas platumu (m): "))
    
    
    istabas_laukums = istabas_garums * istabas_platums
    print(f"Istabas laukums: {istabas_laukums:.2f} m2")
    
    
    nepieciešamais_pakas_skaits = -(-istabas_laukums // pakas_sedzosa_platiba)  # Apaļojam uz augšu
    print(f"Nepieciešamais pakas skaits: {nepieciešamais_pakas_skaits:.0f} pakas")
    
  
    kopējās_izmaksas = nepieciešamais_pakas_skaits * pakas_cena
    print(f"Kopējās izmaksas: {kopējās_izmaksas:.2f} EUR")
    
    
    nepieciešamais_plaksnu_skaits = nepieciešamais_pakas_skaits * plaksnu_skaits_paka
    print(f"Kopējais plākšņu skaits: {nepieciešamais_plaksnu_skaits} gab.")
    
   
    print("\nUzklāšanas zīmējuma izvēle:")
    print("1 - 1 - 1")
    print("½ - 1 - 1")
    print("2/3 - 1 - 1\n")
    uzklasanas_sh = input("Izvēlieties uzklāšanas zīmējumu (piem., '1 - 1 - 1'): ")
    print(f"Jūsu izvēlētais zīmējums: {uzklasanas_sh}")


laminata_izmaksas()
