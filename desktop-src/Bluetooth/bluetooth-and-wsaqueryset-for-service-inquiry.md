---
title: Bluetooth e WSAQUERYSET per la richiesta di assistenza
description: Utilizzo della struttura WSAQUERYSET con le funzioni WSALookupServiceBegin e WSALookupServiceNext per ottenere informazioni sul processo di richiesta del servizio.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth e WSAQUERYSET per richieste di Bluetooth
- WSAQUERYSET Bluetooth , per la richiesta di assistenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5db9c6cc3b6cc49f968c4eb39821b8b9857b0df
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467098"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>Bluetooth e WSAQUERYSET per la richiesta di assistenza

Bluetooth usa la struttura [**WSAQUERYSET,**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) con varie funzioni, per facilitare l'individuazione di dispositivi e servizi nello spazio dei nomi Bluetooth, NS \_ BTH.

Le [**funzioni WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usano la struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) per ottenere dati sul processo di richiesta del servizio. Nella tabella seguente viene descritto come impostare i valori dei membri nella **struttura WSAQUERYSET** a questo scopo.




| Membro | Input per WSALookupServiceBegin | Valore restituito da WSALookupServiceNext | 
|--------|--------------------------------|------------------------------------------|
| <strong>dwSize</strong> | Deve essere impostato su <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>). | <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) restituito dal sistema. | 
| <strong>dwOutputFlags</strong> | Non usato. | Non usato. | 
| <strong>lpszServiceInstanceName</strong> | Non usato. | Nome visualizzato del servizio, convertito come stringa con codifica UTF-8 dalla codifica della lingua predefinita del Bluetooth ServiceName SDP. Restituito se LUP_RETURN_NAME specificato. | 
| <strong>lpServiceClassId</strong> | Obbligatorio. L'UUID Bluetooth specifico per i servizi per i quali viene eseguita la ricerca. Ad esempio, se questo valore è impostato sull'UUID del protocollo L2CAP, restituisce tutti i servizi che usano il protocollo L2CAP nel dispositivo di destinazione. Se impostato sull'UUID di un servizio specifico, restituirà solo le istanze di tale servizio. | Non usato. | 
| <strong>lpVersion</strong> | Non usato. | Non usato. | 
| <strong>lpszComment</strong> | Non usato. | Descrizione del servizio, convertita come stringa con codifica UTF-8 dalla codifica della lingua predefinita dell'Bluetooth ServiceDescription SDP. Restituito se <strong>LUP_RETURN_COMMENT</strong> specificato. | 
| <strong>dwNameSpace</strong> | Deve essere NS_BTH. | Restituisce NS_BTH. | 
| <strong>lpNSProviderId</strong> | Non usato. | Non usato. | 
| <strong>lpszContext</strong> | Obbligatorio. Indirizzo Bluetooth dispositivo con cui stabilire una connessione SDP ed eseguire una query per i servizi. Questo valore deve essere una stringa convertita tramite la chiamata di funzione <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString.</strong></a> Se viene specificato l Bluetooth del dispositivo locale, viene cercato il database SDP locale. | Non usato. | 
| <strong>dwNumberOfProtocols</strong> | Non usato. | Non usato. | 
| <strong>lpafpProtocols</strong> | Non usato. | Non usato. | 
| <strong>lpszQueryString</strong> | Non usato. | Non usato. | 
| <strong>dwNumberOfCsAddrs</strong> | Non usato. | Indica il numero di elementi nella matrice <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>di</strong></a> CSADDR_INFO strutture . | 
| <strong>lpcsaBuffer</strong> | Non usato. | Puntatore a <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>una struttura CSADDR_INFO</strong></a> il cui membro <strong>LocalAddr.lpSockaddr</strong> punta a un <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH che</strong></a> contiene l'indirizzo collegabile completo del servizio remoto, convertito dalla prima voce dell'attributo SDP Bluetooth ProtocolDescriptorList. Restituito se <strong>LUP_RETURN_ADDR</strong> specificato. | 
| <strong>lpBlob</strong> | facoltativo. Puntatore a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> struttura che contiene parametri avanzati per limitare i risultati della ricerca. Se specificato, <strong>lpServiceClassId viene</strong> ignorato e le query memorizzate nella cache non hanno esito positivo. | <ul><li>Se viene eseguita una ricerca del servizio: puntatore a una <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>struttura BLOB</strong></a> che restituisce gli handle del servizio. (<strong>BLOB.cbSize</strong>)/<strong>sizeof</strong>(ULONG) calcola il numero di handle. <strong>BLOB.pBlobData</strong> è una matrice di valori ULONG che rappresentano gli handle del servizio.</li><li>Se viene eseguita una ricerca di attributo o serviceAttribute: puntatore a una <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>struttura BLOB</strong></a> che restituisce il record SDP binario. <strong>BLOB.cbSize è</strong> la dimensione del record SDP binario. <strong>BLOB.pBlobData</strong> punta al record stesso. Il record SDP binario è necessario in molti casi perché solo un numero limitato di attributi SDP può essere convertito nella struttura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> e vengono convertite solo le stringhe UTF-8 codificate predefinite. Le funzioni per facilitare l'analisi del record SDP binario sono disponibili nella Bluetooth <a href="bluetooth-reference.md">informazioni di riferimento.</a></li><li>Restituito se LUP_RETURN_BLOB specificato.</li></ul> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bluetooth e WSAQUERYSET per Set Service](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth e WSAQUERYSET per la richiesta di dispositivi](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Bluetooth e BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

Bluetooth e WSALookupServiceNext
</dt> <dt>

[Bluetooth Riferimento](bluetooth-reference.md)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**BTH \_ QUERY \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
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

 

 
