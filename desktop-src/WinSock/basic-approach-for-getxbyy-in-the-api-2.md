---
description: La maggior parte delle funzioni getXbyY viene convertita dalla sequenza Ws232.dll in una sequenza \_ WSALookupServiceBegin, WSALookupServiceNext e WSALookupServiceEnd che usa uno di un set di GUID speciali come classe del servizio.
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: Approccio di base per GetXbyY nell'API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9e6dd0e5569bd11de813e28eaec1ee04f6b5f206277f695cdb9aaab05ec4a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322625"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a>Approccio di base per GetXbyY nell'API

La maggior parte delle funzioni **getXbyY** viene convertita dal32.dll Ws2 in una sequenza \_ [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)e [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) che usa uno di un set di GUID speciali come classe del servizio. Questi GUID identificano il tipo di **operazione getXbyY** che viene emulata. La query è vincolata ai provider di servizi dei nomi che supportano AF \_ INET. Ogni volta che una funzione **getXbyY** restituisce una struttura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) o [**SERVENT,**](/windows/desktop/api/winsock/ns-winsock-servent) il32.dll Ws2 specifica il \_ flag BLOB LUP \_ RETURN in \_ **WSALookupServiceBegin** in modo che le informazioni desiderate vengono restituite dal provider di servizi dei nomi. Queste strutture devono essere modificate leggermente perché i puntatori contenuti all'interno devono essere sostituiti con offset relativi all'inizio dei dati del BLOB. Tutti i valori a cui fanno riferimento questi parametri del puntatore devono ovviamente essere completamente contenuti nel BLOB e tutte le stringhe sono ASCII.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrazione e risoluzione dei nomi](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



