---
description: La query WSALookupServiceBegin USA SVCID \_ inet \_ SERVICEBYNAME come GUID della classe del servizio.
ms.assetid: 72ee4a10-2864-48e3-a72c-ae069eb5aef3
title: Funzioni getservbyname e getservbyport in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd910dc7ab478c262bd5ca6c480dc3ec58e1b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129187"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-spi"></a>Funzioni getservbyname e getservbyport in SPI

La query [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) USA SVCID \_ inet \_ SERVICEBYNAME come GUID della classe del servizio. Il parametro *lpszServiceInstanceName* fa riferimento a una stringa che indica il nome del servizio o la porta del servizio e, facoltativamente, il protocollo del servizio. La formattazione della stringa è illustrata come FTP/TCP o 21/TCP o solo FTP. La stringa non distingue tra maiuscole e minuscole. La barra contrassegnata, se presente, separa l'identificatore del protocollo dalla parte precedente della stringa. Il \_32.dll WS2 specifica il \_ BLOB restituito LUP \_ e NSP inserisce una struttura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) nel BLOB (usando gli offset invece dei puntatori come descritto in precedenza). Rete deve rispettare anche questi altri \_ \_ \* flag di LUP restituiti.



| Flag              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_nome restituito \_ LUP | Restituisce il membro del **\_ nome s** dalla struttura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) in *lpszServiceInstanceName*.                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_tipo restituito \_ LUP | Restituisce il GUID canonico in *lpServiceClassId* . si comprende che un servizio identificato come FTP o 21 può trovarsi in un'altra porta secondo le convenzioni stabilite localmente. Il membro della **\_ porta s** della struttura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) deve indicare la posizione in cui il servizio può essere contattato nell'ambiente locale. Il GUID canonico restituito quando \_ \_ è impostato il tipo restituito LUP deve essere uno dei GUID predefiniti di Svcs. h che corrisponde al numero di porta indicato nella struttura **SERVENT** . |



 

 

 



