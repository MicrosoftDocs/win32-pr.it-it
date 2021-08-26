---
title: Gestione degli errori delle applicazioni server
description: Se l'applicazione server elabora correttamente il file caricato, l'applicazione deve restituire 200.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c66654bdc0070bf5988d16ac2489d62dc3614b44156337747052df5c7c314e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005281"
---
# <a name="handling-server-application-errors"></a>Gestione degli errori delle applicazioni server

Se l'applicazione server elabora correttamente il file caricato, l'applicazione deve restituire 200. Se l'applicazione non restituisce 200, il client BITS usa il codice di errore per determinare se l'errore è temporaneo o irreversibile.

Tutti i codici di errore 3xx sono errori temporanei tranne 300- 305 e 307, che sono errori irreversibili. Tutti i codici di errore 4xx sono errori irreversibili, ad eccezione degli errori 408 e 409, che sono errori temporanei. Tutti i codici di errore 5xx sono errori temporanei tranne 501 e 505, che sono errori irreversibili. Tutti gli altri codici HTTP sono considerati errori temporanei. Si noti che un codice di errore 403 è l'unico codice di errore che impedisce a BITS di pubblicare nuovamente il file di caricamento nell'applicazione server.

Per recuperare l'errore, chiamare [**il metodo IBackgroundCopyError::GetError.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) Il contesto di errore sarà BG \_ ERROR \_ CONTEXT REMOTE \_ \_ APPLICATION.

 

 




