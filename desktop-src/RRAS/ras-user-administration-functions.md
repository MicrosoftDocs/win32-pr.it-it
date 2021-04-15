---
title: Funzioni di amministrazione utenti RAS
description: Usare le funzioni seguenti per gestire gli utenti di connessione remota
ms.assetid: e58fa4a6-16d3-4953-bf21-887d08e25af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf8c1e7df962eff2064dac06da256f3a78e8ed17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473998"
---
# <a name="ras-user-administration-functions"></a>Funzioni di amministrazione utenti RAS

Usare le funzioni seguenti per gestire gli utenti di connessione remota:

-   [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)
-   [**MprAdminSendUserMessage**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)
-   [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)
-   [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)

Per ottenere un elenco di utenti correnti in un particolare dominio, usare la funzione [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) . Il prototipo per questa funzione si trova nel file di intestazione lmaccess. h.

 

 