---
title: Collegamento alla DLL di Accesso remoto
description: Se un'applicazione si collega in modo statico alla DLL RASAPI32, l'applicazione non verrà caricata se il servizio di accesso remoto non è installato.
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b98757320cf9a166e741eb10ace8607d0287740a5494ca20fcc431b16b4367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790651"
---
# <a name="linking-to-the-remote-access-dll"></a>Collegamento alla DLL di Accesso remoto

Se un'applicazione si collega in modo statico alla DLL RASAPI32, l'applicazione non verrà caricata se il servizio di accesso remoto non è installato. Un'applicazione RAS può essere caricata quando RAS non è installato usando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) per caricare la DLL e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per ottenere puntatori alle funzioni RAS.

Le funzioni RAS si trovano in RASAPI32.DLL. La libreria di importazione per queste funzioni è RASAPI32. Lib. Per usare le funzioni RAS, i programmi devono includere i file seguenti:



| File       | Descrizione                                                                 |
|------------|-----------------------------------------------------------------------------|
| Ras. H      | Contiene i prototipi di funzione RAS, le costanti e le definizioni di struttura. |
| RASERROR. H | Contiene i codici di errore RAS.                                               |



 

 

 