---
title: Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo
description: Questo argomento descrive come usare la funzione WSALookupServiceBegin per eseguire una richiesta di dispositivi visibili e fantasma. Per altre informazioni, vedere Individuazione Bluetooth dispositivi e servizi.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth e WSALookupServiceBegin per la richiesta di Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4423b7c1c27124771c518409d9d1393a5f83afb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469188"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a>Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo

Questo argomento descrive come usare la funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) per eseguire una richiesta di dispositivi visibili e fantasma. Per altre informazioni, vedere [Individuazione Bluetooth dispositivi e servizi.](discovering-bluetooth-devices-and-services.md)

La [**funzione WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) usa una struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) nel primo parametro, *lpqsRestrictions*, per definire i criteri di ricerca. Bluetooth linee guida specifiche per l'uso della **funzione WSALookupServiceBegin** e **di WSAQUERYSET.**

Nella tabella seguente sono elencate le restrizioni che si applicano alla struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) passata al parametro *lpqsRestrictions* durante l'esecuzione di query per i dispositivi.




| Membro WSAQUERYSET | Restrizione | 
|--------------------|-------------|
| <strong>dwSize</strong> | Impostare su <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>). | 
| <strong>lpBlob</strong> | Questo membro contiene un puntatore facoltativo a una <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>struttura</strong></a> BLOB. Se questo membro viene specificato, i parametri di richiesta del dispositivo validi per <strong>LUP_FLUSHCACHE</strong> sono i seguenti:<ul><li>Il <strong>membro cbSize</strong> della struttura <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> deve essere <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</li><li>Il <strong>membro pBlobData</strong> è un puntatore a una struttura <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE,</strong></a> per cui il membro <strong>LAP</strong> è il codice di accesso alla richiesta di Bluetooth e il membro length è la lunghezza, in secondi, della richiesta. <strong></strong></li></ul> | 
| <strong>dwNameSpace</strong> | Impostare su <strong>NS_BTH</strong>. | 
| Altri membri | Gli altri membri della <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>struttura WSAQUERYSET</strong></a> vengono ignorati. | 




 

I flag elencati nella tabella seguente vengono usati nel *parametro dwControlFlags* per controllare i risultati della query. I flag **LUP \_ CONTAINERS** e **LUP \_ FLUSHCACHE** vengono usati dalla funzione [**WSALookupServiceBegin.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) Il resto dei flag viene usato nelle chiamate alla funzione [**WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)

| Contrassegno               | Risultato                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONTENITORI \_ LUP    | Specifica che lo scopo della query è ottenere un elenco Bluetooth dispositivi e non un elenco di servizi. Questo flag deve essere impostato.                                                                                                                                                                                                                                                                                       |
| LUP \_ FLUSHCACHE    | Attiva una richiesta di dispositivi locali o fa in modo che i risultati memorizzati nella cache delle query precedenti siano restituiti.                                                                                                                                                                                                                                                                                                                |
| TIPO \_ RESTITUITO \_ LUP  | Restituire il Bluetooth COD (classe di bit del dispositivo) direttamente nel membro **lpServiceClassId** della [**struttura WSAQUERYSET.**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) Il codice COD viene mappato al **membro Data1** del GUID.                                                                                                                                                                                                      |
| LUP \_ RES \_ SERVICE  | Restituisce le informazioni per l'indirizzo Bluetooth locale. Questo flag ha effetto solo se **viene specificato anche LUP RETURN \_ \_ ADDR.**                                                                                                                                                                                                                                                                                       |
| NOME \_ RESTITUITO \_ LUP  | Restituisce il nome visualizzato del dispositivo nel membro **lpszServiceInstanceName** della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) per ogni chiamata alla [**funzione WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) Questo flag deve essere specificato  anche per recuperare il membro del nome della [**struttura BTH \_ DEVICE \_ INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) quando si specifica il flag **LUP RETURN \_ \_ BLOB.** |
| LUP \_ RETURN \_ ADDR  | Restituisce una struttura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) che contiene l'indirizzo a 48 bit del peer nel membro **lpcsaBuffer** della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) per ogni chiamata alla funzione [**WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) Gli altri membri nella **struttura SOCKADDR \_ BTH** saranno vuoti.                                                            |
| BLOB \_ RESTITUITO LUP \_  | Restituisce la [**struttura BTH \_ DEVICE \_ INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) in ogni chiamata successiva a [**WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)                                                                                                                                                                                                                                                           |
| LUP \_ FLUSHPREVIOUS | Ignorare il successivo dispositivo disponibile e restituire il dispositivo che lo segue.                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bluetooth e WSALookupServiceBegin per l'individuazione del servizio](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth e WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth e WSAQUERYSET per la richiesta di dispositivi](bluetooth-and-wsaqueryset-for-device-inquiry.md)
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

[**BTH \_ QUERY \_ DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 
