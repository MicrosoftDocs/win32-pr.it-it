---
description: PNRP utilizza la struttura WSAQUERYSET insieme a diverse funzioni per semplificare la risoluzione dei nomi e l'enumerazione di nomi e cloud.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP e WSAQUERYSET (P2P. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d09d135d57af0922feb5a143c41696d85dac083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314740"
---
# <a name="pnrp-and-wsaqueryset"></a>PNRP e WSAQUERYSET

PNRP utilizza la struttura [**WSAQUERYSET**](winsock-nsp-reference-links.md) insieme a diverse funzioni per semplificare la risoluzione dei nomi e l'enumerazione di nomi e cloud.

Per le definizioni complete delle funzioni [**WSAQUERYSET**](winsock-nsp-reference-links.md) o Windows Sockets, vedere le rispettive definizioni nella documentazione dell'API di Windows Sockets 2 in Platform SDK.

## <a name="wsaqueryset-and-wsasetservice"></a>WSAQUERYSET e WSASetService

La funzione [**WSASetService**](winsock-nsp-reference-links.md) usa la struttura **WSAQUERYSET** per registrare o rimuovere i nomi dei peer. La pagina [PNRP e WSASetService](pnrp-and-wsasetservice.md) illustra come usare la struttura **WSAQUERYSET** con questa funzione.

## <a name="wsaqueryset-and-wsalookupservicebegin"></a>WSAQUERYSET e WSALookupServiceBegin

La struttura [**WSAQUERYSET**](winsock-nsp-reference-links.md) viene utilizzata ampiamente con le funzioni **WSALookupServiceBegin**, **WSALookupServiceNext** e **WSALookupServiceEnd** . Le pagine di riferimento seguenti illustrano in dettaglio il modo in cui queste funzioni usano la struttura **WSAQUERYSET** :

-   [PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
-   [PNRP e WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
-   [PNRP e WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                             |
| Versione<br/>                  | Windows XP con SP1 con Advanced Networking Pack per Windows XP<br/>  |
| Intestazione<br/>                   | <dl> <dt>P2P. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PNRP e BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP e WSASetService](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




