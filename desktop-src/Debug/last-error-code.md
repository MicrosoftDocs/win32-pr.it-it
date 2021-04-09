---
description: Quando si verifica un errore, la maggior parte delle funzioni di sistema restituisce un codice di errore, in genere 0, NULL o &\# 8211; 1.
ms.assetid: fd5b0d6e-78cf-4f51-b61d-d32576cd485a
title: Codice Last-Error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bf0fe2f544fc3d87690be81b0d09767745ef95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965973"
---
# <a name="last-error-code"></a>Codice Last-Error

Quando si verifica un errore, la maggior parte delle funzioni di sistema restituisce un codice di errore, in genere 0, **null** o-1. Molte funzioni di sistema impostano inoltre un codice di errore aggiuntivo denominato *ultimo codice di errore*. Questo codice di errore viene mantenuto separatamente per ogni thread in esecuzione. un errore in un thread non sovrascrive il codice dell'ultimo errore in un altro thread. Qualsiasi funzione può chiamare la funzione [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) o [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex) per impostare il codice dell'ultimo errore per il thread corrente. Queste funzioni sono destinate principalmente alle librerie di collegamento dinamico (DLL), in modo che possano fornire informazioni all'applicazione chiamante. Si noti che alcune funzioni chiamano **SetLastError** o **SetLastErrorEx** con 0 quando hanno esito positivo, cancellando il codice di errore impostato dalla funzione non riuscita più di recente, mentre altri no.

Un'applicazione può recuperare il codice dell'ultimo errore utilizzando la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) ; il codice di errore può indicare altre informazioni su ciò che si è verificato in realtà perché la funzione ha esito negativo. La documentazione per le funzioni di sistema indicherà le condizioni in base alle quali la funzione imposta il codice dell'ultimo errore.

Il sistema definisce un set di codici di errore che possono essere impostati come ultimi codici di errore o restituiti da queste funzioni. I codici di errore sono valori a 32 bit (il bit 31 è il bit più significativo). Il bit 29 è riservato ai codici di errore definiti dall'applicazione; Questo bit non è impostato per nessun codice di errore di sistema. Se si definiscono i codici di errore per l'applicazione, impostare questo bit per indicare che il codice di errore è stato definito da un'applicazione e per assicurarsi che i codici di errore non siano in conflitto con i codici di errore definiti dal sistema. Per ulteriori informazioni, vedere WinError. h e [codici di errore di sistema](system-error-codes.md).

 

 
