---
description: Quando si verifica un errore, la maggior parte delle funzioni di sistema restituisce un codice di errore, in genere 0, NULL o &\# 8211;1.
ms.assetid: fd5b0d6e-78cf-4f51-b61d-d32576cd485a
title: Last-Error code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd3f7a202f4ed67105620a7d2688cfa278fbdc127ed942861de0d69517e96620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912551"
---
# <a name="last-error-code"></a>Last-Error code

Quando si verifica un errore, la maggior parte delle funzioni di sistema restituisce un codice di errore, in genere 0, **NULL** o -1. Molte funzioni di sistema impostano anche un codice di errore aggiuntivo denominato *ultimo codice di errore.* Questo codice di errore viene gestito separatamente per ogni thread in esecuzione. un errore in un thread non sovrascrive l'ultimo codice di errore in un altro thread. Qualsiasi funzione può chiamare la [**funzione SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) o [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex) per impostare il codice dell'ultimo errore per il thread corrente. Queste funzioni sono destinate principalmente alle librerie a collegamento dinamico (DLL), in modo che possano fornire informazioni all'applicazione chiamante. Si noti che alcune funzioni chiamano **SetLastError** o **SetLastErrorEx** con 0 quando hanno esito positivo, mentre altre no.

Un'applicazione può recuperare il codice dell'ultimo errore usando [**la funzione GetLastError.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) Il codice di errore può indicare altre informazioni su ciò che si è effettivamente verificato per fare in modo che la funzione non riesca. La documentazione per le funzioni di sistema indicherà le condizioni in cui la funzione imposta l'ultimo codice di errore.

Il sistema definisce un set di codici di errore che possono essere impostati come codici di ultimo errore o restituiti da queste funzioni. I codici di errore sono valori a 32 bit (il bit 31 è il bit più significativo). Il bit 29 è riservato ai codici di errore definiti dall'applicazione. nessun codice di errore di sistema ha questo bit impostato. Se si definiscono codici di errore per l'applicazione, impostare questo bit per indicare che il codice di errore è stato definito da un'applicazione e per assicurarsi che i codici di errore non siano in conflitto con i codici di errore definiti dal sistema. Per altre informazioni, vedere WinError.h e Codici [di errore di sistema.](system-error-codes.md)

 

 
