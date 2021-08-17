---
title: Funzioni di amministrazione utente RAS
description: Usare le funzioni seguenti per gestire gli utenti remoti
ms.assetid: e58fa4a6-16d3-4953-bf21-887d08e25af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be0965a2befbe8a52ff91c2a1323a0455072fbe696d29f5a3cbb15e40e3b7c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789133"
---
# <a name="ras-user-administration-functions"></a>Funzioni di amministrazione utente RAS

Usare le funzioni seguenti per gestire gli utenti remoti:

-   [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)
-   [**MprAdminSendUserMessage**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)
-   [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)
-   [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)

Per ottenere un elenco degli utenti correnti in un determinato dominio, usare la [**funzione NetQueryDisplayInformation.**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) Il prototipo per questa funzione si trova nel file di intestazione lmaccess.h.

 

 