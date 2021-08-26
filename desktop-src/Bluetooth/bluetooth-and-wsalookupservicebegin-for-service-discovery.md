---
title: Bluetooth e WSALookupServiceBegin per l'individuazione dei servizi
description: Per individuare l'esistenza di un particolare servizio in un server Bluetooth, i client usano le funzioni WSALookupServiceBegin, WSALookupServiceNext e WSALookupServiceEnd.
ms.assetid: d9961600-cdca-42ec-92eb-118b8186ed2e
keywords:
- Bluetooth e WSALookupServiceBegin per Service Discovery Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30049adfb02fb6478e581e4a6fdefdfe5b6960bdbc872f30be5fe482a28ac541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004251"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-service-discovery"></a>Bluetooth e WSALookupServiceBegin per l'individuazione dei servizi

Per individuare l'esistenza di un particolare servizio in un server Bluetooth, i client usano le funzioni [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)e [**WSALookupServiceEnd.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) Le query possono essere eseguite per gli indirizzi locali e remoti, ma le connessioni possono essere stabilite solo con indirizzi remoti. Gli handle del servizio individuati durante questa operazione non possono essere usati per eliminare il servizio [**tramite WSASetService.**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) Il loopback non è supportato da RFCOMM.

È possibile eseguire due tipi di base di query di individuazione dei servizi:

-   Query per uno o più servizi nel dispositivo locale
-   Query per uno o più servizi in un dispositivo peer specificato

La [**funzione WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) riceve una struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) nel parametro *lpqsRestrictions.* **WSALookupServiceBegin** esegue una query client in base al set di restrizioni di ricerca contenute in **WSAQUERYSET.** Bluetooth client devono specificare le restrizioni elencate nella tabella seguente nella struttura **WSAQUERYSET** quando si usa la funzione **WSALookupServiceBegin** per eseguire query sui servizi.



| Membro WSAQUERYSET    | Restrizione                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**            | Impostare su **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                                                                                                                                                                                                    |
| **lpServiceClassId**  | Impostare sul valore più specifico Bluetooth UUID che può essere usato per determinare l'ambito della query. Ad esempio, se **si imposta lpServiceClassId** sull'UUID del protocollo L2CAP, vengono restituiti tutti i servizi L2CAP, essenzialmente enumerando tutti i record SD nella destinazione. L'impostazione dell'UUID su un servizio specifico, tuttavia, restituisce solo le istanze di tale servizio.<br/> |
| **dwNameSpace**       | Impostare su **NS \_ BTH.**                                                                                                                                                                                                                                                                                                                                                             |
| **dwNumberOfCsAddrs** | Impostare su 0.                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszContext**       | Impostare sull'Bluetooth dispositivo con cui stabilire una connessione SDP per eseguire la query dei servizi. Questo membro deve essere una stringa convertita tramite la [**funzione WSAAddressToString.**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Se viene fornito l'indirizzo radio locale, viene cercata la ricerca nei record SDP locali.<br/>                                             |
| Altri membri         | Tutti gli altri membri della [**struttura WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) vengono ignorati.                                                                                                                                                                                                                                                                                        |



 

La connessione SDP al dispositivo remoto non rimane attiva dopo che la [**funzione WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ha completato una query del servizio. la connessione viene terminata prima che **venga restituito WSALookupServiceBegin.** Le applicazioni che richiedono che la connessione SDP rimanga attiva dopo il completamento di una query del servizio devono specificare l'UUID della classe di servizio a cui connettersi usando il membro **serviceClassId** della struttura [**\_ BTH SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) quando viene eseguita la chiamata di funzione Windows Sockets [**Connect.**](/windows/desktop/api/winsock2/nf-winsock2-connect)

I flag elencati nella tabella seguente vengono usati nel parametro *dwControlFlags* delle funzioni [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) per controllare i risultati della query. I flag **LUP \_ CONTAINERS** e **LUP \_ FLUSHCACHE** vengono usati dalla funzione **WSALookupServiceBegin.** Il resto dei flag viene usato nelle chiamate alla **funzione WSALookupServiceNext.**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Contrassegno</th>
<th>Risultato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>LUP_CONTAINERS</strong></td>
<td>Non deve essere impostato.</td>
</tr>
<tr class="even">
<td><strong>LUP_FLUSHCACHE</strong></td>
<td>Le applicazioni devono in genere <strong>specificare LUP_FLUSHCACHE</strong>. Questo flag indica al sistema di ignorare le informazioni memorizzate nella cache e stabilire una connessione SDP over-the-air al dispositivo specificato per eseguire la ricerca SDP. Questa operazione non memorizzata nella cache può richiedere alcuni secondi(mentre una ricerca memorizzata nella cache restituisce rapidamente). Bluetooth attualmente non memorizza nella cache in modo proattivo i record SDP dai dispositivi vicini, né memorizza nella cache le query precedenti in modo aggressivo. Pertanto, le applicazioni devono prevedere che le query potrebbero non restituire alcun risultato (con codice di errore <strong>WSASERVICE_NOT_FOUND</strong>) se LUP_FLUSHCACHE <strong>non</strong> è specificato. I dati memorizzati nella cache disponibili tramite l'Windows Sockets possono essere migliorati in futuro.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RES_SERVICE</strong></td>
<td>Restituisce informazioni sull'indirizzo Bluetooth locale. Questo flag ha effetto solo <strong>se</strong> LUP_RETURN_ADDR è specificato anche .</td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_NAME</strong></td>
<td>Restituisce il nome visualizzato del servizio nel membro <strong>lpszServiceInstanceName</strong> della struttura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> per ogni chiamata alla <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>funzione WSALookupServiceNext.</strong></a></td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_TYPE</strong></td>
<td>Restituire l'ID della classe del servizio <strong>nel membro lpServiceClassId</strong> della <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>struttura WSAQUERYSET.</strong></a>
<blockquote>
[!Note]<br />
L'uso di questo flag è applicabile solo alla <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina"><strong>funzione WSALookupServiceBegin.</strong></a> Questo valore è sempre zero per <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_ADDR</strong></td>
<td>Restituisce un indirizzo nel <strong>membro lpcsaBuffer</strong> da usare con le <a href="/windows/desktop/api/winsock2/nf-winsock2-connect"><strong>chiamate di</strong></a> funzione connect. L'indirizzo restituito contiene il numero di porta.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_BLOB</strong></td>
<td>Restituisce i record SD corrispondenti nel membro <strong>lpBlob,</strong> formattati in base alla specifica Bluetooth record SDP.</td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_ALL</strong></td>
<td>Restituisce tutte le informazioni sui flag precedenti.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_COMMENT</strong></td>
<td>Restituire la descrizione del servizio nel membro <strong>lpszComment</strong> della struttura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> per ogni chiamata alla <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>funzione WSALookupServiceNext.</strong></a></td>
</tr>
<tr class="even">
<td><strong>LUP_FLUSHPREVIOUS</strong></td>
<td>Ignorare il record disponibile successivo e restituire il record che lo segue.</td>
</tr>
</tbody>
</table>



 

## <a name="advanced-service-queries"></a>Query di servizio avanzate

Le operazioni di query descritte nella sezione precedente possono essere usate per restituire tutti i risultati da un singolo GUID, che dovrebbe essere sufficiente per la maggior parte delle applicazioni. Una query avanzata consente a un'applicazione di creare una query più specifica. fornisce la possibilità di trovare corrispondenze tra UUID e attributi nelle informazioni restituite.

Per eseguire una query avanzata per i servizi, Bluetooth client devono specificare le restrizioni seguenti nella struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) passata nel parametro *lpqsRestrictions.*



| Membro WSAQUERYSET   | Restrizione                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**           | Impostare su **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                                                                                                                                                        |
| **lpszContext**      | Impostare sull'Bluetooth dispositivo con cui stabilire una connessione SDP per eseguire la query dei servizi. Questo membro deve essere una stringa convertita tramite la [**funzione WSAAddressToString.**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Se viene fornito l'indirizzo radio locale, viene cercata la ricerca nei record SDP locali.<br/> |
| **lpBlob.pBlobData** | Puntatore a [**una struttura BTH \_ QUERY \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) che contiene tutti i parametri che limitano i risultati della query.                                                                                                                                                                                           |
| **dwNameSpace**      | Impostare su **NS \_ BTH.**                                                                                                                                                                                                                                                                                                                 |
| Altri membri        | Tutti gli altri membri della [**struttura WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) vengono ignorati.                                                                                                                                                                                                                                            |



 

I flag seguenti vengono passati nel *parametro dwControlFlags* di [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) per controllare i risultati di una query avanzata.

| Contrassegno                     | Risultato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CONTENITORI \_ LUP**      | Non deve essere impostato.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **LUP \_ FLUSHCACHE**      | Le applicazioni devono in genere **specificare LUP \_ FLUSHCACHE**. Questo flag indica al sistema di ignorare le informazioni memorizzate nella cache e stabilire una connessione SDP over-the-air al dispositivo specificato per eseguire la ricerca SDP. Questa operazione non memorizzata nella cache può richiedere alcuni secondi(mentre una ricerca memorizzata nella cache restituisce rapidamente). Bluetooth memorizza nella cache in modo proattivo i record SDP dai dispositivi vicini, né memorizza nella cache in modo aggressivo le query precedenti. Le applicazioni devono pertanto prevedere che le query non restituiranno spesso alcun risultato (**WSASERVICE \_ NOT \_ FOUND**) se **LUP \_ FLUSHCACHE** non è specificato. I dati memorizzati nella cache disponibili tramite l'Windows Sockets possono essere migliorati in futuro. |
| **SERVIZIO LUP \_ RES \_**    | Restituisce informazioni per l'indirizzo Bluetooth locale. L'impostazione di questo flag ha effetto solo se **viene specificato anche LUP RETURN \_ \_ ADDRR.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **NOME \_ RESTITUITO \_ LUP**    | Restituisce il nome visualizzato del servizio. Questo flag viene ignorato per **SDP \_ SERVICE SEARCH \_ \_ REQUEST**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **TIPO \_ RESTITUITO \_ LUP**    | Restituisce l'ID della classe del servizio. Questo flag viene ignorato per **SDP \_ SERVICE SEARCH \_ \_ REQUEST**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **LUP \_ RETURN \_ ADDR**    | Restituisce un indirizzo nel membro **lpcsaBuffer** da usare con le [**chiamate di**](/windows/desktop/api/winsock2/nf-winsock2-connect) funzione connect. L'indirizzo restituito contiene il numero di porta. Questo flag viene ignorato per **SDP \_ SERVICE SEARCH \_ \_ REQUEST**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **BLOB \_ RESTITUITO LUP \_**    | Restituisce i record SD corrispondenti in un formato conforme alla specifica Bluetooth record SDP. Per **SDP \_ SERVICE SEARCH \_ \_ REQUEST,** il risultato in **lpBlob** per la chiamata successiva a [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) è una matrice Bluetooth handle SDP. Per **SDP \_ SERVICE ATTRIBUTE \_ \_ REQUEST** e **SDP SERVICE SEARCH ATTRIBUTE \_ \_ \_ \_ REQUEST**, il risultato per ogni chiamata successiva a **WSALookupServiceNext** è un record SDP Bluetooth binario i cui attributi sono limitati a quelli specificati dal **membro pRange** della query. Questo flag è obbligatorio per **SDP \_ SERVICE SEARCH \_ \_ REQUEST**.                                                               |
| **COMMENTO \_ RESTITUITO \_ LUP** | Restituisce la descrizione del servizio nel membro **lpszComment** della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) per ogni chiamata alla [**funzione WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **LUP \_ FLUSHPREVIOUS**   | Ignorare il successivo record disponibile e restituire il record che lo segue.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

Nell'input **lpBlob** -> **pBlobData** punta a una [**struttura BTH QUERY \_ \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) che contiene i valori elencati nella tabella seguente.

> [!Note]  
> La richiesta di ricerca iniziale deve essere in grado di rientrare in un pacchetto L2CAP. La risposta, tuttavia, può essere suddivisa in molti pacchetti L2CAP.

 



| Membro            | Valore                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**          | Tipo di ricerca da eseguire. Questo valore può essere uno dei valori **di SDP \_ SERVICE SEARCH \_ \_ REQUEST**, **SDP SERVICE ATTRIBUTE \_ \_ \_ REQUEST** o **SDP SERVICE SEARCH ATTRIBUTE \_ \_ \_ \_ REQUEST**. Ogni tipo di ricerca è associato a un meccanismo di ricerca sottostante definito dalla specifica Bluetooth SDP. Ogni risultato restituito è nel formato descritto dalla struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) definita in precedenza in questa sezione (Advanced Service Queries). |
| **serviceHandle** | Usato per le ricerche di attributi. Questo valore specifica l'handle del servizio con cui eseguire una query degli attributi nel **membro pRange.**                                                                                                                                                                                                                                                                                                                                            |
| **UUID**         | Usato per le ricerche **service e serviceAttribute.** Questo valore specifica gli UUID che un record deve contenere per corrispondere alla ricerca. Se è necessario eseguire query su UUID minori di **MAX \_ UUIDS \_ IN \_ QUERY,** questo valore imposta l'elemento SdpQueryUuid che segue immediatamente l'ultimo UUID valido su tutti gli zeri.                                                                                                                                                                       |
| **numRange**      | Usato per le ricerche di **attributi e serviceAttribute.** Questo valore specifica il numero di elementi in **pRange.**                                                                                                                                                                                                                                                                                                                                                             |
| **pRange**        | Usato per le ricerche di **attributi e serviceAttribute.** Questo valore specifica i valori degli attributi da recuperare per tutti i record corrispondenti.                                                                                                                                                                                                                                                                                                                                        |



 

Dopo ogni chiamata riuscita alla funzione [**WSALookupServiceNext,**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) **lpBlob** -> **pBlobData** punta a un blocco di dati che contiene i valori elencati nella tabella seguente.

| Valore                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RICHIESTA DI RICERCA DEL SERVIZIO SDP \_ \_ \_**                                                    | Matrice di handle di record SDP identica a **ServiceRecordHandleList** definita da Bluetooth 1.1 SDP 4.5.2. Il numero di handle SDP restituiti viene calcolato da (**lpBlob**->cbSize)/**sizeof**(ULONG). Tutti i risultati vengono restituiti in una singola chiamata alla [**funzione WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) |
| **SDP \_ RICHIESTA \_ \_ DELL'ATTRIBUTO DEL** SERVIZIO O **RICHIESTA \_ DELL'ATTRIBUTO \_ DI RICERCA DEL \_ \_ SERVIZIO SDP** | Oggetto binario Bluetooth record SDP. Per **SDP \_ SERVICE ATTRIBUTE \_ \_ REQUEST,** tutti i risultati vengono restituiti in una singola chiamata alla [**funzione WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)                                                                                                                                                       |



 

> [!Note]  
> Se il membro **lpBlob** non viene specificato durante l'input per una query del servizio, viene eseguita una ricerca di servizi e attributi per il servizio specificato nel membro **lpServiceClassId** sugli attributi da 0 a 0xFFFF.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bluetooth e WSAQUERYSET per richiesta di servizio](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[Individuazione di dispositivi e servizi Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth e WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[**BTH \_ QUERY \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**connettersi**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

