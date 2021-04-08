---
title: Bluetooth e WSAQUERYSET per la richiesta di assistenza
description: Uso della struttura WSAQUERYSET con le funzioni WSALookupServiceBegin e WSALookupServiceNext per ottenere informazioni sul processo di richiesta del servizio.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth e WSAQUERYSET per richieste di assistenza Bluetooth
- WSAQUERYSET Bluetooth, per la richiesta di assistenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656fa407829112005c9c54c5ab84c9c1bf2f4e33
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732202"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>Bluetooth e WSAQUERYSET per la richiesta di assistenza

Bluetooth usa la struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , con varie funzioni, per facilitare l'individuazione di dispositivi e servizi nello spazio dei nomi Bluetooth, NS \_ BTH.

Le funzioni [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usano la struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) per ottenere i dati sul processo di richiesta del servizio. La tabella seguente descrive come impostare i valori dei membri nella struttura **WSAQUERYSET** a questo scopo.



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
<td>Nome visualizzato del servizio, convertito come stringa con codifica UTF-8 dalla codifica della lingua predefinita dell'attributo Bluetooth ServiceName SDP. Restituito se viene specificato LUP_RETURN_NAME.</td>
</tr>
<tr class="even">
<td><strong>lpServiceClassId</strong></td>
<td>Obbligatorio. UUID del singolo Bluetooth più specifico per i servizi per i quali viene eseguita la ricerca. Se, ad esempio, questo valore è impostato sull'UUID del protocollo L2CAP, restituisce tutti i servizi usando il protocollo L2CAP sul dispositivo di destinazione. Se impostato sull'UUID di un servizio specifico, restituirà solo le istanze di tale servizio.</td>
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
<td>Descrizione del servizio, convertita come stringa con codifica UTF-8 dalla codifica della lingua predefinita dell'attributo Bluetooth ServiceDescription SDP. Restituito se viene specificato <strong>LUP_RETURN_COMMENT</strong> .</td>
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
<td>Obbligatorio. Indirizzo del dispositivo Bluetooth con cui stabilire una connessione SDP ed eseguire query per i servizi. Questo valore deve essere una stringa convertita tramite la chiamata di funzione <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> . Se viene fornito l'indirizzo del dispositivo Bluetooth locale, viene eseguita la ricerca nel database SDP locale.</td>
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
<td>Indica il numero di elementi nella matrice di strutture di <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>lpcsaBuffer</strong></td>
<td>Non usato.</td>
<td>Puntatore a una struttura <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> il cui membro <strong>LocalAddr. lpSockaddr</strong> fa riferimento a un <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> che contiene l'indirizzo di connessione completo del servizio remoto, convertito dalla prima voce dell'attributo Bluetooth ProtocolDescriptorList SDP. Restituito se viene specificato <strong>LUP_RETURN_ADDR</strong> .</td>
</tr>
<tr class="odd">
<td><strong>lpBlob</strong></td>
<td>facoltativo. Puntatore a una struttura <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> che contiene parametri avanzati per limitare i risultati della ricerca. Se specificato, <strong>lpServiceClassId</strong> viene ignorato e le query memorizzate nella cache non vengono eseguite correttamente.</td>
<td><ul>
<li>Se viene eseguita la ricerca di un servizio: puntatore a una struttura <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> che restituisce gli handle del servizio. (<strong>BLOB. cbSize</strong>)/<strong>sizeof</strong>(ulong) calcola il numero di handle. <strong>BLOB. pBlobData</strong> è una matrice di valori ULONG che rappresenta gli handle del servizio.</li>
<li>Se viene eseguito un attributo o una ricerca serviceAttribute: puntatore a una struttura <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> che restituisce il record SDP binario. <strong>BLOB. cbSize</strong> è la dimensione del record SDP binario. <strong>BLOB. pBlobData</strong> punta al record stesso. Il record SDP binario è necessario in molti casi perché solo un numero limitato di attributi SDP può essere convertito nella struttura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> e vengono convertite solo le stringhe UTF-8 codificate predefinite. Le funzioni per semplificare l'analisi del record SDP binario sono disponibili nella sezione di <a href="bluetooth-reference.md">riferimento Bluetooth</a> .</li>
<li>Restituito se viene specificato LUP_RETURN_BLOB.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bluetooth e WSAQUERYSET per il servizio set](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth e WSAQUERYSET per la richiesta del dispositivo](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Bluetooth e BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

Bluetooth e WSALookupServiceNext
</dt> <dt>

[Informazioni di riferimento su Bluetooth](bluetooth-reference.md)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_servizio query \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**\_informazioni CSADDR**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**\_BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 