URL --> https://web2-lab6-library-app.onrender.com

Feature list:

interpolation/one-way binding --> Da, u vise navrata, npr.src/App.vue :11, ili src/components/BookDetails.vue :5, :6, :7
two-way binding --> Da, src/components/SpotReservation.vue :4
methods --> Da, src/components/Announcement.vue, :43-:58
computed properties --> Da, src/components/Announcement.vue, :33-:41
barem jedan scoped style  --> Da, src/components/SpotReservation.vue :28-:54
koristiti barem jedan lifecycle hook --> Da, src/views/HomeView.vue :41-:44
routing (više stranica) --> Da, navedeno dolje specificno, ruter implementiran ovdi: /src/router/index.js
	- aplikacija mora biti bookmarkable, tako da rade linkovi (ne samo na root, već i moj-web.com/stranica1, moj-web.com/stranica2) 
   		Da, radi za 3 rute - home(/), catalogue(/catalogue) i rules(/rules)
   - dinamičko usmjeravanje s 404 stranicom ("catch all")
   		Da, implementirano ovdi /src/router/index.js :27-:31, probati s bilo kojom drugom rutom, npr /fake-route
(barem) dvije komponente --> Da, implementirane su 4 u src/components
	- komponenta bez stanja, koristiti properties --> u src/components/SpotReservation.vue :12-:14
	- komponenta sa stanjem --> Da, u src/components/Announcement.vue :27-:32
barem jedna komponenta mora emitirati barem jedan event --> da, u src/components/SpotReservation.vue :12-:14
store (Pinia) --> Da, u src/components/Announcement.vue :18, :37-:40, :49-:52 + implementiran store u src/stores/announcementStore.js cijeli file
asinkroni dohvat podataka s backenda --> Da, u src/views/HomeView.vue :46-:70, koristio se Mockey

Napomena: Postoji jedan console.error log, ali on je ostavljen namjerno - kod ucitavanja slika naslova knjiga namjerno je dan krivi link, 
				a sve s namjerom da se pokaze kako je implementiran recovery od takvog ponasanja
            - moze se rekreirati tako da se otvori /catalogue ruta i tamo se loada nepostojeca slika od knjige 'Pride and prejudice'
            - rezultat je da se ucita fallback slika umjesto te nepostojece
               	- implementirano u library-app/src/components/BookDetails.vue :41-:44





