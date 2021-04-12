---
description: La maggior parte delle funzioni getXbyY vengono convertite dal \_32.dll WS2 in una sequenza WSALookupServiceBegin, WSALookupServiceNext e WSALookupServiceEnd che usa uno di un set di GUID speciali come classe del servizio.
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: Approccio di base per GetXbyY nell'API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4c038c87d6eb6e7ab2a4476271662d5b9567ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526208"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a>Approccio di base per GetXbyY nell'API

La maggior parte delle funzioni **getXbyY** vengono convertite dal \_32.dll WS2 in una sequenza [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)e [**WSALOOKUPSERVICEEND**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) che usa uno di un set di GUID speciali come classe del servizio. Questi GUID identificano il tipo di operazione **getXbyY** da emulare. La query è vincolata a questi provider di servizi dei nomi che supportano AF \_ inet. Ogni volta che una funzione **getXbyY** restituisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) o [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) , WS2 \_32.dll specifica il \_ flag del BLOB restituito LUP \_ in **WSALookupServiceBegin** in modo che le informazioni desiderate vengano restituite dal provider di servizi del nome. Queste strutture devono essere modificate leggermente in quanto i puntatori contenuti in devono essere sostituiti da offset relativi all'inizio dei dati del BLOB. Tutti i valori a cui fanno riferimento questi parametri del puntatore devono, ovviamente, essere completamente contenuti all'interno del BLOB e tutte le stringhe sono ASCII.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrazione e risoluzione dei nomi](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



