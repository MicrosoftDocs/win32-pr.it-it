---
title: Collegamento alla DLL di accesso remoto
description: Se un'applicazione è collegata in modo statico alla DLL RASAPI32, l'applicazione non verrà caricata se il servizio di accesso remoto non è installato.
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd8b29eab4bf2cd7689836e9310a3c0f6370dfb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872781"
---
# <a name="linking-to-the-remote-access-dll"></a>Collegamento alla DLL di accesso remoto

Se un'applicazione è collegata in modo statico alla DLL RASAPI32, l'applicazione non verrà caricata se il servizio di accesso remoto non è installato. È possibile caricare un'applicazione RAS quando RAS non è installato utilizzando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) per caricare la dll e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per ottenere i puntatori alle funzioni RAS.

Le funzioni RAS si trovano in RASAPI32.DLL. La libreria di importazione per queste funzioni è RASAPI32. LIB. Per utilizzare le funzioni RAS, i programmi devono includere i seguenti file:



| File       | Descrizione                                                                 |
|------------|-----------------------------------------------------------------------------|
| Ras. H      | Contiene i prototipi di funzione RAS, le costanti e le definizioni della struttura. |
| RASERROR. H | Contiene i codici di errore RAS.                                               |



 

 

 