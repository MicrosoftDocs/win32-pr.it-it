---
title: Gestione degli errori dell'applicazione server
description: Se l'applicazione server elabora correttamente il file caricato, l'applicazione deve restituire 200.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6019f296cb3b960369efc2c3ca8f25eb7738e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707855"
---
# <a name="handling-server-application-errors"></a>Gestione degli errori dell'applicazione server

Se l'applicazione server elabora correttamente il file caricato, l'applicazione deve restituire 200. Se l'applicazione non restituisce 200, il client BITS usa il codice di errore per determinare se l'errore è un errore temporaneo o un errore irreversibile.

Tutti i codici di errore di 3xx sono errori temporanei tranne 300-305 e 307, che sono errori irreversibili. Tutti i codici di errore di 4xx sono errori irreversibili ad eccezione di 408 e 409, che sono errori temporanei. Tutti i codici di errore di 5xx sono errori temporanei tranne 501 e 505, che sono errori irreversibili. Tutti gli altri codici HTTP sono considerati errori temporanei. Si noti che un codice di errore 403 è l'unico codice di errore che impedisce a BITS di pubblicare nuovamente il file di caricamento nell'applicazione server.

Per recuperare l'errore, chiamare il metodo [**IBackgroundCopyError:: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) . Il contesto di errore sarà \_ applicazione remota del contesto di errore BG \_ \_ \_ .

 

 




