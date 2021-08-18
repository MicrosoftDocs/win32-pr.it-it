---
description: PNRP usa la struttura WSAQUERYSET in combinazione con varie funzioni per facilitare la risoluzione dei nomi e l'enumerazione di nomi e cloud.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP e WSAQUERYSET (P2P.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bbc635b0c1ca19cfaeeeb7f8b013aefad1e49e2141dd9715a36c0238e7be6f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061358"
---
# <a name="pnrp-and-wsaqueryset"></a>PNRP e WSAQUERYSET

PNRP usa la [**struttura WSAQUERYSET**](winsock-nsp-reference-links.md) in combinazione con varie funzioni per facilitare la risoluzione dei nomi e l'enumerazione di nomi e cloud.

Per le definizioni complete [**delle funzioni WSAQUERYSET**](winsock-nsp-reference-links.md) o Windows Sockets, vedere le rispettive definizioni nella documentazione dell'API Windows Sockets 2 in Platform SDK.

## <a name="wsaqueryset-and-wsasetservice"></a>WSAQUERYSET e WSASetService

La [**funzione WSASetService**](winsock-nsp-reference-links.md) usa la **struttura WSAQUERYSET** per registrare o rimuovere i nomi peer. La [pagina PNRP e WSASetService](pnrp-and-wsasetservice.md) illustra come usare la struttura **WSAQUERYSET** con questa funzione.

## <a name="wsaqueryset-and-wsalookupservicebegin"></a>WSAQUERYSET e WSALookupServiceBegin

La struttura [**WSAQUERYSET**](winsock-nsp-reference-links.md) viene usata ampiamente con le funzioni **WSALookupServiceBegin**, **WSALookupServiceNext** e **WSALookupServiceEnd.** I dettagli sull'uso della struttura **WSAQUERYSET** da parte di queste funzioni sono dettagliati nelle pagine di riferimento seguenti:

-   [PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
-   [PNRP e WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
-   [PNRP e WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                             |
| Versione<br/>                  | Windows XP con SP1 con Advanced Networking Pack per Windows XP<br/>  |
| Intestazione<br/>                   | <dl> <dt>P2P.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PNRP e BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP e WSASetService](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




