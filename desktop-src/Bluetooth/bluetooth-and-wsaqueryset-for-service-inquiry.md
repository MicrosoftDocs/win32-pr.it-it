---
title: Bluetooth e WSAQUERYSET per la richiesta di assistenza
description: Uso della struttura WSAQUERYSET con le funzioni WSALookupServiceBegin e WSALookupServiceNext per ottenere informazioni sul processo di richiesta del servizio.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth e WSAQUERYSET per la richiesta di Bluetooth
- WSAQUERYSET Bluetooth , per la richiesta del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38bd953f8d205f0afb097ec2d098ee674a01d5fc37cfbaf4109e02cdbb4b395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959160"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>Bluetooth e WSAQUERYSET per la richiesta di assistenza

Bluetooth usa la struttura [**WSAQUERYSET,**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) con varie funzioni, per facilitare l'individuazione di dispositivi e servizi nello spazio dei nomi Bluetooth, NS \_ BTH.

Le [**funzioni WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usano la struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) per ottenere dati sul processo di richiesta del servizio. Nella tabella seguente viene descritto come impostare i valori dei membri nella **struttura WSAQUERYSET** a questo scopo.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Membro</th>
<th>Input per WSALookupServiceBegin</th>
<th>Valore restituito da WSALookupServiceNext</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>dwSize</strong></td>
<td>Deve essere impostato su <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</td>
<td><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) restituito dal sistema.</td>
</tr>
<tr class="even">
<td><strong>dwOutputFlags</strong></td>
<td>Non usato.</td>
<td>Non usato.</td>
</tr>
<tr class="odd">
<td><strong>lpszServiceInstanceName</strong></td>
<td>Non usato.</td>
<td>Nome visualizzato del servizio, convertito come stringa con codifica UTF-8 dalla codifica della lingua predefinita dell'attributo SDP Bluetooth ServiceName. Restituito se LUP_RETURN_NAME specificato.</td>
</tr>
<tr class="even">
<td><strong>lpServiceClassId</strong></td>
<td>Obbligatorio. Il singolo oggetto Bluetooth UUID per i servizi per cui viene eseguita la ricerca. Ad esempio, se questo valore è impostato sull'UUID del protocollo L2CAP, restituisce tutti i servizi che usano il protocollo L2CAP nel dispositivo di destinazione. Se impostato sull'UUID di un servizio specifico, restituirebbe solo le istanze di tale servizio.</td>
<td>Non usato.</td>
</tr>
<tr class="odd">
<td><strong>lpVersion</strong></td>
<td>Non usato.</td>
<td>Non usato.</td>
</tr>
<tr class="even">
<td><strong>lpszComment</strong></td>
<td>Non usato.</td>
<td>Descrizione del servizio, convertita come stringa con codifica UTF-8 dalla codifica della lingua predefinita dell'attributo SDP Bluetooth ServiceDescription. Restituito se <strong>LUP_RETURN_COMMENT</strong> specificato.</td>
</tr>
<tr class="odd">
<td><strong>dwNameSpace</strong></td>
<td>Deve essere NS_BTH.</td>
<td>Restituisce NS_BTH.</td>
</tr>
<tr class="even">
<td><strong>lpNSProviderId</strong></td>
<td>Non usato.</td>
<td>Non usato.</td>
</tr>
<tr class="odd">
<td><strong>lpszContext</strong></td>
<td>Obbligatorio. Indirizzo Bluetooth dispositivo con cui stabilire una connessione SDP ed eseguire query per i servizi. Questo valore deve essere una stringa convertita tramite la chiamata di funzione <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString.</strong></a> Se viene specificato l Bluetooth del dispositivo locale, viene cercato il database SDP locale.</td>
<td>Non usato.</td>
</tr>
<tr class="even">
<td><strong>dwNumberOfProtocols</strong></td>
<td>Non usato.</td>
<td>Non usato.</td>
</tr>
<tr class="odd">
<td><strong>lpafpProtocols</strong></td>
<td>Non usato.</td>
<td>Non usato.</td>
</tr>
<tr class="even">
<td><strong>lpszQueryString</strong></td>
<td>Non usato.</td>
<td>Non usato.</td>
</tr>
<tr class="odd">
<td><strong>dwNumberOfCsAddrs</strong></td>
<td>Non usato.</td>
<td>Indica il numero di elementi nella matrice <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>di</strong></a> CSADDR_INFO strutture.</td>
</tr>
<tr class="even">
<td><strong>lpcsaBuffer</strong></td>
<td>Non usato.</td>
<td>Puntatore a una <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>struttura CSADDR_INFO</strong></a> il cui membro <strong>LocalAddr.lpSockaddr</strong> punta a un <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH che</strong></a> contiene l'indirizzo connettebile completo del servizio remoto, convertito dalla prima voce dell'attributo SDP Bluetooth ProtocolDescriptorList. Restituito se <strong>LUP_RETURN_ADDR</strong> specificato.</td>
</tr>
<tr class="odd">
<td><strong>lpBlob</strong></td>
<td>facoltativo. Puntatore a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> struttura che contiene parametri avanzati per limitare i risultati della ricerca. Se specificato, <strong>lpServiceClassId</strong> viene ignorato e le query memorizzate nella cache non hanno esito positivo.</td>
<td><ul>
<li>Se viene eseguita una ricerca del servizio: puntatore a una <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>struttura BLOB</strong></a> che restituisce gli handle del servizio. (<strong>BLOB.cbSize</strong>)/<strong>sizeof</strong>(ULONG) calcola il numero di handle. <strong>BLOB.pBlobData</strong> è una matrice di valori ULONG che rappresentano gli handle del servizio.</li>
<li>Se viene eseguita una ricerca di attributo o serviceAttribute: puntatore a una <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>struttura BLOB</strong></a> che restituisce il record SDP binario. <strong>BLOB.cbSize è</strong> la dimensione del record SDP binario. <strong>BLOB.pBlobData</strong> punta al record stesso. Il record SDP binario è necessario in molti casi perché solo un numero limitato di attributi SDP può essere convertito nella struttura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> e vengono convertite solo le stringhe UTF-8 codificate predefinite. Le funzioni per facilitare l'analisi del record SDP binario sono disponibili nella Bluetooth <a href="bluetooth-reference.md">riferimento.</a></li>
<li>Restituito se LUP_RETURN_BLOB specificato.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bluetooth e WSAQUERYSET per il servizio Set](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth e WSAQUERYSET per la richiesta dei dispositivi](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Bluetooth e BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

Bluetooth e WSALookupServiceNext
</dt> <dt>

[Bluetooth Riferimento](bluetooth-reference.md)
</dt> <dt>

[**Blob**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**SERVIZIO QUERY BTH \_ \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**CSADDR \_ INFO**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 