---
description: La query WSALookupServiceBegin usa SVCID \_ HOSTNAME come GUID della classe di servizio.
ms.assetid: 6f073e1a-2985-4e94-8174-94b1fcaf13d1
title: Funzione gethostname nell'spi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b610016222ab8a06ed874377be9ae447ad1d194ab9605a6e07b3cf829f520093
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132264"
---
# <a name="gethostname-function-in-the-spi"></a>Funzione gethostname nell'spi

La query [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ HOSTNAME come GUID della classe di servizio. Se *lpszServiceInstanceName* è Null o fa riferimento a una stringa Null , ovvero . ""), l'host locale deve essere risolto. In caso contrario, viene eseguita una ricerca su un nome host specificato. Ai fini dell'emulazione di [**gethostname,**](/windows/desktop/api/winsock/nf-winsock-gethostname) il32.dll Ws2 specifica un puntatore Null per lpszServiceInstanceName e specifica LUP RETURN NAME in modo che il nome host sia restituito nel \_  \_ parametro \_ *lpszServiceInstanceName.* Se un'applicazione usa questa query e specifica LUP \_ RETURN \_ ADDR, l'indirizzo host verrà fornito in una **struttura CSADDR \_ INFO.** L'azione \_ \_ LUP RETURN BLOB non è definita per questa query. Per impostazione predefinita, le informazioni sulla porta saranno pari a zero, a meno che *lpszQueryString* non faccia riferimento a un servizio come ftp, nel qual caso verrà fornito l'indirizzo di trasporto completo del servizio indicato.

 

 



