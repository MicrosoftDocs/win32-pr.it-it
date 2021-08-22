---
description: La maggior parte delle funzioni GetXbyY viene convertita da Ws232.dll in una sequenza \_ WSALookupServiceBegin, WSALookupServiceNext, WSALookupServiceEnd che usa uno di un set di GUID speciali come classe del servizio.
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: Approccio di base per GetXbyY nello spi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba707747dd6082bfa6c8b3c4dd3c19e8d6ce968359745947227ee464d97f984f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560525"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a>Approccio di base per GetXbyY nello spi

La maggior parte delle funzioni **GetXbyY** viene convertita da Ws232.dll in una sequenza \_ [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) che usa uno di un set di GUID speciali come classe del servizio. Questi GUID identificano il tipo **di operazione GetXbyY** che viene emulata. La query è vincolata ai server di rete che supportano AF \_ INET. Ogni volta che una funzione **GetXbyY** restituisce una struttura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) o [**SERVENT,**](/windows/desktop/api/winsock/ns-winsock-servent) il32.dll Ws2 specificherà il \_ flag BLOB LUP \_ RETURN in \_ **WSALookupServiceBegin** in modo che le informazioni desiderate verranno restituite dal provider di servizi di rete. Queste strutture devono essere modificate leggermente perché i puntatori contenuti all'interno devono essere sostituiti con offset relativi all'inizio dei dati del BLOB. Tutti i valori a cui fanno riferimento questi membri puntatore devono ovviamente essere completamente contenuti nel BLOB e tutte le stringhe sono ASCII.

 

 



