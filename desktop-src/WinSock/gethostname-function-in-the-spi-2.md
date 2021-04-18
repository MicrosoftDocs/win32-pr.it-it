---
description: La query WSALookupServiceBegin usa il \_ nome host SVCID come GUID della classe del servizio.
ms.assetid: 6f073e1a-2985-4e94-8174-94b1fcaf13d1
title: Funzione gethostname in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9aef10be48b264eb607184caf38bd687a5fe307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306966"
---
# <a name="gethostname-function-in-the-spi"></a>Funzione gethostname in SPI

La query [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa il \_ nome host SVCID come GUID della classe del servizio. Se *lpszServiceInstanceName* è null o fa riferimento a una stringa null (ovvero. ""), l'host locale deve essere risolto. In caso contrario, verrà eseguita una ricerca in un nome host specificato. Ai fini dell'emulazione di [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) , il WS2 \_32.dll specifica un puntatore null per *lpszServiceInstanceName* e specifica LUP \_ nome restituito \_ in modo che il nome host venga restituito nel parametro *lpszServiceInstanceName* . Se un'applicazione usa questa query e specifica LUP \_ return \_ addr, l'indirizzo host verrà fornito in una struttura **di \_ informazioni di CSADDR** . L' \_ azione LUP return \_ BLOB non è definita per questa query. Le informazioni sulla porta verranno automaticamente azzerate a meno che *lpszQueryString* faccia riferimento a un servizio quale FTP, nel qual caso verrà fornito l'indirizzo di trasporto completo del servizio indicato.

 

 



