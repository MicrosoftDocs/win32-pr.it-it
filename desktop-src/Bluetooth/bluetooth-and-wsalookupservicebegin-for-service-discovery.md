---
title: Bluetooth e WSALookupServiceBegin per l'individuazione del servizio
description: Per individuare l'esistenza di un servizio specifico su un server Bluetooth, i client utilizzano le funzioni WSALookupServiceBegin, WSALookupServiceNext e WSALookupServiceEnd.
ms.assetid: d9961600-cdca-42ec-92eb-118b8186ed2e
keywords:
- Bluetooth e WSALookupServiceBegin per l'individuazione del servizio Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274b3beb3de7683bd43a0f99350db6e1a347f51e
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103873062"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-service-discovery"></a>Bluetooth e WSALookupServiceBegin per l'individuazione del servizio

Per individuare l'esistenza di un servizio specifico su un server Bluetooth, i client utilizzano le funzioni [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)e [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) . È possibile eseguire query per indirizzi locali e remoti, ma le connessioni possono essere stabilite solo con indirizzi remoti. Gli handle del servizio individuati durante questa operazione non possono essere utilizzati per eliminare il servizio tramite [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea). Il loopback non è supportato da RFCOMM.

È possibile eseguire due tipi di query di individuazione dei servizi:

-   Query per uno o più servizi nel dispositivo locale
-   Esegue una query per uno o più servizi in un dispositivo peer specificato

La funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) riceve una struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) nel parametro *lpqsRestrictions* . **WSALookupServiceBegin** esegue una query client basata sul set di restrizioni di ricerca contenute in **WSAQUERYSET** . I client Bluetooth devono specificare le restrizioni, elencate nella tabella seguente, nella struttura **WSAQUERYSET** quando si usa la funzione **WSALookupServiceBegin** per eseguire una query per i servizi.



| Membro WSAQUERYSET    | Restrizione                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**            | Impostare su **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                                                                                                                                                                                                    |
| **lpServiceClassId**  | Impostare sull'UUID Bluetooth più specifico che può essere utilizzato per determinare l'ambito della query. Se, ad esempio, si imposta **lpServiceClassId** sull'UUID del protocollo L2CAP, vengono restituiti tutti i servizi L2CAP, in sostanza l'enumerazione di tutti i record SD nella destinazione. Se si imposta l'UUID su un servizio specifico, tuttavia, vengono restituite solo le istanze di tale servizio.<br/> |
| **dwNameSpace**       | Impostare su **NS \_ BTH**.                                                                                                                                                                                                                                                                                                                                                             |
| **dwNumberOfCsAddrs** | Impostare su 0.                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszContext**       | Impostare sull'indirizzo del dispositivo Bluetooth con cui stabilire una connessione SDP per eseguire la query dei servizi. Questo membro deve essere una stringa convertita mediante la funzione [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) . Se viene specificato l'indirizzo di radio locale, viene eseguita la ricerca dei record SDP locali.<br/>                                             |
| Altri membri         | Tutti gli altri membri della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) vengono ignorati.                                                                                                                                                                                                                                                                                        |



 

La connessione SDP al dispositivo remoto non rimane attiva dopo che la funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ha completato una query del servizio. la connessione viene terminata prima della restituzione di **WSALookupServiceBegin** . Le applicazioni che richiedono la connessione SDP rimangano attive dopo il completamento di una query del servizio devono specificare l'UUID della classe del servizio a cui connettersi usando il membro **serviceClassId** della struttura [**\_ BTH di SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) durante l'emissione della chiamata di funzione Windows Sockets [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) .

I flag, elencati nella tabella seguente, vengono usati nel parametro *dwControlFlags* delle funzioni [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) per controllare i risultati della query. I **flag \_ LUP** e **LUP \_ FlushCache** vengono usati dalla funzione **WSALookupServiceBegin** ; i restanti flag vengono usati nelle chiamate alla funzione **WSALookupServiceNext** .

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
<td>In genere, le applicazioni devono specificare <strong>LUP_FLUSHCACHE</strong>. Questo flag indica al sistema di ignorare le informazioni memorizzate nella cache e di stabilire una connessione SDP in aria al dispositivo specificato per eseguire la ricerca SDP. Questa operazione non memorizzata nella cache può richiedere alcuni secondi (mentre una ricerca memorizzata nella cache restituisce rapidamente). Attualmente Bluetooth non memorizza nella cache in modo proattivo i record SDP dai dispositivi nelle vicinanze, né attualmente memorizza nella cache in modo aggressivo le query precedenti. Pertanto, le applicazioni devono prevedere che le query non restituiscono alcun risultato (con un codice di errore <strong>WSASERVICE_NOT_FOUND</strong>) se non è specificato <strong>LUP_FLUSHCACHE</strong> . I dati memorizzati nella cache disponibili tramite l'interfaccia Windows Sockets possono essere migliorati in futuro.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RES_SERVICE</strong></td>
<td>Restituisce informazioni sull'indirizzo Bluetooth locale. Questo flag ha effetto solo se viene specificato anche <strong>LUP_RETURN_ADDR</strong> .</td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_NAME</strong></td>
<td>Restituisce il nome visualizzato del servizio nel membro <strong>lpszServiceInstanceName</strong> della struttura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> per ogni chiamata alla funzione <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> .</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_TYPE</strong></td>
<td>Restituisce l'ID della classe del servizio nel membro <strong>lpServiceClassId</strong> della struttura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> .
<blockquote>
[!Note]<br />
L'uso di questo flag è applicabile solo alla funzione <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina"><strong>WSALookupServiceBegin</strong></a> . Questo valore è sempre zero per <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_ADDR</strong></td>
<td>Restituisce un indirizzo nel membro <strong>lpcsaBuffer</strong> da utilizzare con le chiamate di funzione <a href="/windows/desktop/api/winsock2/nf-winsock2-connect"><strong>Connect</strong></a> . L'indirizzo restituito contiene il numero di porta.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_BLOB</strong></td>
<td>Restituisce i record SD corrispondenti nel membro <strong>lpBlob</strong> , formattati in base alla specifica del record Bluetooth SDP.</td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_ALL</strong></td>
<td>Restituisce tutte le informazioni sui flag precedenti.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_COMMENT</strong></td>
<td>Restituisce la descrizione del servizio nel membro <strong>lpszComment</strong> della struttura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> per ogni chiamata alla funzione <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>LUP_FLUSHPREVIOUS</strong></td>
<td>Ignorare il record successivo disponibile e restituire il record che lo segue.</td>
</tr>
</tbody>
</table>



 

## <a name="advanced-service-queries"></a>Query di servizio avanzate

Le operazioni di query descritte nella sezione precedente possono essere utilizzate per restituire tutti i risultati da un singolo GUID, che dovrebbe essere sufficiente per la maggior parte delle applicazioni. Una query avanzata consente a un'applicazione di creare una query più specifica; offre la possibilità di associare UUID e attributi alle informazioni restituite.

Per eseguire una query avanzata per i servizi, i client Bluetooth devono specificare le restrizioni seguenti nella struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) che viene passata al parametro *lpqsRestrictions* .



| Membro WSAQUERYSET   | Restrizione                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**           | Impostare su **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                                                                                                                                                        |
| **lpszContext**      | Impostare sull'indirizzo del dispositivo Bluetooth con cui stabilire una connessione SDP per eseguire la query dei servizi. Questo membro deve essere una stringa convertita mediante la funzione [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) . Se viene specificato l'indirizzo di radio locale, viene eseguita la ricerca dei record SDP locali.<br/> |
| **lpBlob. pBlobData** | Puntatore a una struttura del [**\_ \_ servizio query BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) che contiene tutti i parametri che limitano i risultati della query.                                                                                                                                                                                           |
| **dwNameSpace**      | Impostare su **NS \_ BTH**.                                                                                                                                                                                                                                                                                                                 |
| Altri membri        | Tutti gli altri membri della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) vengono ignorati.                                                                                                                                                                                                                                            |



 

I flag seguenti vengono passati nel parametro *dwControlFlags* di [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) per controllare i risultati di una query avanzata.

| Contrassegno                     | Risultato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_contenitori LUP**      | Non deve essere impostato.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **\_FlushCache LUP**      | Le applicazioni in genere devono specificare **LUP \_ FlushCache**. Questo flag indica al sistema di ignorare le informazioni memorizzate nella cache e di stabilire una connessione SDP in aria al dispositivo specificato per eseguire la ricerca SDP. Questa operazione non memorizzata nella cache può richiedere alcuni secondi (mentre una ricerca memorizzata nella cache restituisce rapidamente). Bluetooth non memorizza nella cache in modo proattivo i record SDP dai dispositivi nelle vicinanze, né memorizza nella cache aggressiva le query precedenti. Pertanto, le applicazioni devono prevedere che le query non restituiscano spesso risultati (**WSASERVICE \_ non \_ trovato**) se **LUP \_ FlushCache** non è specificato. I dati memorizzati nella cache disponibili tramite l'interfaccia Windows Sockets possono essere migliorati in futuro. |
| **\_servizio LUP res \_**    | Restituisce informazioni per l'indirizzo Bluetooth locale. L'impostazione di questo flag ha effetto solo se viene specificato anche **LUP \_ return \_ addrer** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **\_nome restituito \_ LUP**    | Restituisce il nome visualizzato del servizio. Questo flag viene ignorato per **la \_ \_ \_ richiesta di ricerca del servizio SDP**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **\_tipo restituito \_ LUP**    | Restituisce l'ID della classe del servizio. Questo flag viene ignorato per **la \_ \_ \_ richiesta di ricerca del servizio SDP**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **LUP \_ restituire \_ addr**    | Restituisce un indirizzo nel membro **lpcsaBuffer** da utilizzare con le chiamate di funzione [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) . L'indirizzo restituito contiene il numero di porta. Questo flag viene ignorato per **la \_ \_ \_ richiesta di ricerca del servizio SDP**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **\_BLOB restituito \_ LUP**    | Restituire i record SD corrispondenti in un formato conforme alla specifica del record Bluetooth SDP. Per **la \_ \_ \_ richiesta di ricerca del servizio SDP**, il risultato in **LpBlob** per la chiamata successiva a [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) è una matrice di handle di SDP Bluetooth. Per la richiesta di attributi del **\_ servizio \_ \_ SDP** e la **richiesta di attributo di \_ ricerca del servizio \_ \_ \_ SDP**, il risultato per ogni chiamata successiva a **WSALookupServiceNext** è un record di tipo SDP binario Bluetooth i cui attributi sono limitati a quelli specificati dal membro **Prange** della query. Questo flag è obbligatorio per **la \_ \_ \_ richiesta di ricerca del servizio SDP**.                                                               |
| **LUP \_ \_ Commento restituito** | Restituisce la descrizione del servizio nel membro **lpszComment** della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) per ogni chiamata alla funzione [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **\_FLUSHPREVIOUS LUP**   | Ignorare il record successivo disponibile e restituire il record che lo segue.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

In input **lpBlob** -> **pBlobData** punta a una struttura [**del \_ \_ servizio query BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) che contiene i valori elencati nella tabella seguente.

> [!Note]  
> La richiesta di ricerca iniziale deve essere in grado di rientrare in un pacchetto L2CAP. La risposta, tuttavia, può essere suddivisa in molti pacchetti L2CAP.

 



| Membro            | Valore                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**          | Tipo di ricerca da eseguire. Questo valore può essere una richiesta **di \_ \_ ricerca del \_ servizio SDP**, una richiesta di **\_ attributo del servizio \_ \_ SDP** o una richiesta di **\_ \_ \_ attributo \_ di ricerca** del servizio SDP. Ogni tipo di ricerca è associato a un meccanismo di ricerca sottostante definito dalla specifica Bluetooth SDP. Ogni risultato restituisce il formato descritto dalla struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) definita in precedenza in questa sezione (Advanced Service queries). |
| **serviceHandle** | Utilizzato per le ricerche di attributi. Questo valore specifica l'handle del servizio con il quale eseguire una query sugli attributi del membro **Prange** .                                                                                                                                                                                                                                                                                                                                            |
| **UUID**         | Usato per le ricerche di servizio e **serviceAttribute** . Questo valore specifica gli UUID che un record deve contenere per corrispondere alla ricerca. Se è necessario eseguire query su più UUID per gli UUID **\_ \_ della \_ query** , questo valore imposta l'elemento SdpQueryUuid che segue immediatamente l'ultimo UUID valido a tutti gli zeri.                                                                                                                                                                       |
| **numRange**      | Utilizzato per le ricerche Attribute e **serviceAttribute** . Questo valore specifica il numero di elementi in **Prange**.                                                                                                                                                                                                                                                                                                                                                             |
| **pRange**        | Utilizzato per le ricerche Attribute e **serviceAttribute** . Questo valore specifica i valori di attributo da recuperare per i record corrispondenti.                                                                                                                                                                                                                                                                                                                                        |



 

Dopo ogni chiamata riuscita alla funzione [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) , **lpBlob** -> **pBlobData** punta a un blocco di dati che contiene i valori elencati nella tabella seguente.

| Valore                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_richiesta di \_ ricerca del servizio SDP \_**                                                    | Una matrice di handle di record SDP identici a **ServiceRecordHandleList** definiti da Bluetooth 1,1 SDP 4.5.2. Il numero di handle SDP restituiti viene calcolato da (**lpBlob**->cbSize)/**sizeof**(ulong). Tutti i risultati vengono restituiti in una singola chiamata alla funzione [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . |
| **SDP \_ Richiesta \_ attributo \_ servizio** o **\_ richiesta di \_ \_ attributo di \_ ricerca del servizio SDP** | Un record di SDP Bluetooth binario. Per **la \_ \_ \_ richiesta di attributo del servizio SDP**, tutti i risultati vengono restituiti in una singola chiamata alla funzione [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .                                                                                                                                                       |



 

> [!Note]  
> Se il membro **lpBlob** non viene specificato durante l'input per una query del servizio, viene eseguita una ricerca di un servizio e di un attributo per il servizio specificato nel membro **lpServiceClassId** sugli attributi da 0 a 0xFFFF.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bluetooth e WSAQUERYSET per la richiesta di assistenza](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[Individuazione di dispositivi e servizi Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth e WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[**\_servizio query \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**connessione**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**\_BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
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

