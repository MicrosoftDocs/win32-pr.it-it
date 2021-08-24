---
description: La query WSALookupServiceBegin usa SVCID \_ INET \_ SERVICEBYNAME come GUID della classe di servizio.
ms.assetid: 72ee4a10-2864-48e3-a72c-ae069eb5aef3
title: Funzioni getservbyname e getservbyport in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 466966db2fc605b4043355746a1e606626e3d5d518452d1fab661dcfb68b3238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132164"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-spi"></a>Funzioni getservbyname e getservbyport in SPI

La query [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ INET \_ SERVICEBYNAME come GUID della classe di servizio. Il *parametro lpszServiceInstanceName* fa riferimento a una stringa che indica il nome del servizio o la porta del servizio e (facoltativamente) il protocollo del servizio. La formattazione della stringa è illustrata come ftp/tcp o 21/tcp o semplicemente ftp. La stringa non fa distinzione tra maiuscole e minuscole. La barra, se presente, separa l'identificatore di protocollo dalla parte precedente della stringa. L'32.dll Ws2 specifica LUP RETURN BLOB e il provider di servizi di rete inserirà una struttura SERVENT nel BLOB (usando offset anziché puntatori come descritto in \_ \_ \_ precedenza). [](/windows/desktop/api/winsock/ns-winsock-servent) I server dei criteri di rete devono rispettare anche questi altri flag LUP \_ \_ \* RETURN.



| Flag              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NOME \_ RESTITUITO \_ LUP | Restituisce il **membro \_ del nome s** dalla struttura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) in *lpszServiceInstanceName*.                                                                                                                                                                                                                                                                                                                                                                                                            |
| TIPO \_ RESTITUITO \_ LUP | Restituisce il GUID canonico in *lpServiceClassId* È chiaro che un servizio identificato come ftp o 21 può essere su un'altra porta in base alle convenzioni stabilite localmente. Il **membro di \_ porta s** della [**struttura SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) deve indicare dove è possibile contattare il servizio nell'ambiente locale. Il GUID canonico restituito quando l'opzione LUP RETURN TYPE è impostata deve essere uno dei GUID predefiniti di \_ svcs.h che corrisponde al numero di porta indicato nella struttura \_ **SERVENT.** |



 

 

 



