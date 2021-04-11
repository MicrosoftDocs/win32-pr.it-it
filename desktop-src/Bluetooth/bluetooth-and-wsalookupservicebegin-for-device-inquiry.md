---
title: Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo
description: Questo argomento descrive come usare la funzione WSALookupServiceBegin per eseguire una richiesta di dispositivi visibili e fantasma. Per ulteriori informazioni, vedere Individuazione di dispositivi e servizi Bluetooth.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth e WSALookupServiceBegin per la richiesta di dispositivo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfbcab2a3134289630b4b301390f85e83d1d3d0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104118583"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a>Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo

Questo argomento descrive come usare la funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) per eseguire una richiesta di dispositivi visibili e fantasma. Per ulteriori informazioni, vedere [individuazione di dispositivi e servizi Bluetooth](discovering-bluetooth-devices-and-services.md).

La funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) usa una struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) nel primo parametro, *lpqsRestrictions*, per definire i criteri di ricerca. Bluetooth fornisce linee guida specifiche per l'uso della funzione **WSALookupServiceBegin** e di **WSAQUERYSET**.

La tabella seguente elenca le restrizioni che si applicano alla struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) passata al parametro *lpqsRestrictions* durante l'esecuzione di query per i dispositivi.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Membro WSAQUERYSET</th>
<th>Restrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>dwSize</strong></td>
<td>Impostare su <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</td>
</tr>
<tr class="even">
<td><strong>lpBlob</strong></td>
<td>Questo membro contiene un puntatore facoltativo a una struttura <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> . Se questo membro viene specificato, i parametri validi per la richiesta di informazioni sul dispositivo per <strong>LUP_FLUSHCACHE</strong> sono i seguenti:
<ul>
<li>Il membro <strong>cbSize</strong> della struttura <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> deve essere <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</li>
<li>Il membro <strong>pBlobData</strong> è un puntatore a una struttura di <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> , per cui il membro <strong>lap</strong> è il codice di accesso di richiesta Bluetooth e il membro <strong>length</strong> è la lunghezza, in secondi, dell'indagine.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>dwNameSpace</strong></td>
<td>Impostare su <strong>NS_BTH</strong>.</td>
</tr>
<tr class="even">
<td>Altri membri</td>
<td>Gli altri membri della struttura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> vengono ignorati.</td>
</tr>
</tbody>
</table>



 

I flag elencati nella tabella seguente vengono usati nel parametro *dwControlFlags* per controllare i risultati della query. I **flag \_ LUP** e **LUP \_ FlushCache** vengono usati dalla funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ; i restanti flag vengono usati nelle chiamate alla funzione [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .

| Contrassegno               | Risultato                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_contenitori LUP    | Specifica che lo scopo della query è ottenere un elenco di dispositivi Bluetooth e non un elenco di servizi. Questo flag deve essere impostato.                                                                                                                                                                                                                                                                                       |
| \_FlushCache LUP    | Attiva un'indagine sui dispositivi locali o causa la restituzione dei risultati memorizzati nella cache delle query precedenti.                                                                                                                                                                                                                                                                                                                |
| \_tipo restituito \_ LUP  | Restituisce il MERLUZZo Bluetooth (classe dei bit del dispositivo) direttamente nel membro **lpServiceClassId** della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) . Il MERLUZZo viene mappato al membro **Data1** del GUID.                                                                                                                                                                                                      |
| \_servizio LUP res \_  | Restituisce informazioni per l'indirizzo Bluetooth locale. Questo flag ha effetto solo se viene specificato anche **LUP \_ return \_ addr** .                                                                                                                                                                                                                                                                                       |
| \_nome restituito \_ LUP  | Restituisce il nome visualizzato del dispositivo nel membro **lpszServiceInstanceName** della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) per ogni chiamata alla funzione [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . Questo flag deve essere specificato anche per recuperare il membro del **nome** della struttura di [**\_ \_ informazioni sul dispositivo BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) quando si specifica il flag del **\_ \_ BLOB restituito LUP** . |
| LUP \_ restituire \_ addr  | Restituisce una [**struttura SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) che contiene l'indirizzo a 48 bit del peer nel membro **lpcsaBuffer** della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) per ogni chiamata alla funzione [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . Gli altri membri della struttura **sockaddr \_ BTH** saranno vuoti.                                                            |
| \_BLOB restituito \_ LUP  | Restituisce la struttura delle [**\_ \_ informazioni sul dispositivo BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) per ogni chiamata successiva a [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).                                                                                                                                                                                                                                                           |
| \_FLUSHPREVIOUS LUP | Ignorare il successivo dispositivo disponibile e restituire il dispositivo che lo segue.                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bluetooth e WSALookupServiceBegin per l'individuazione del servizio](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth e WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth e WSAQUERYSET per la richiesta del dispositivo](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Individuazione di dispositivi e servizi Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_dispositivo di query BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**\_BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 