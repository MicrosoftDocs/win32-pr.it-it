---
description: La maggior parte delle funzioni GetXbyY vengono convertite da WS2 \_32.dll a una sequenza WSALookupServiceBegin, WSALookupServiceNext, WSALookupServiceEnd che usa uno di un set di GUID speciali come classe del servizio.
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: Approccio di base per GetXbyY in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d635230bb1c1205d0f6e1aee16fe7c7ac9eab5b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879230"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a>Approccio di base per GetXbyY in SPI

La maggior parte delle funzioni **GetXbyY** vengono convertite da WS2 \_32.dll a una sequenza [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALOOKUPSERVICEEND**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) che usa uno di un set di GUID speciali come classe del servizio. Questi GUID identificano il tipo di operazione **GetXbyY** da emulare. La query è vincolata a tali rete che supportano AF \_ inet. Ogni volta che una funzione **GetXbyY** restituisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) o [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) , l' \_32.dll WS2 specificherà il \_ flag del BLOB restituito LUP \_ in **WSALookupServiceBegin** in modo che le informazioni desiderate vengano restituite da NSP. Queste strutture devono essere modificate leggermente in quanto i puntatori contenuti in devono essere sostituiti da offset relativi all'inizio dei dati del BLOB. Tutti i valori a cui fanno riferimento questi membri del puntatore devono, ovviamente, essere completamente contenuti all'interno del BLOB e tutte le stringhe sono ASCII.

 

 



