---
title: Verifica della registrazione
description: Verifica della registrazione
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee215fd052ffc242900eead069a8b72fd25b31d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955285"
---
# <a name="checking-registration"></a>Verifica della registrazione

Ogni volta che un'applicazione viene caricata, deve controllare la registrazione per determinare quanto segue:

-   Indica se i CLSID sono presenti nel registro di sistema. Se non sono presenti, l'applicazione deve registrarsi come installazione originale.
-   Indica se i CLSID dell'applicazione sono presenti nel registro ma non contengono informazioni correlate a OLE 2. In tal caso, l'applicazione deve registrarsi come installazione originale.
-   Indica se il percorso contenente le voci del server ([LocalServer](localserver.md) e [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) e [InprocServer32](inprocserver32.md)e [DefaultIcon](defaulticon.md)) punta alla posizione in cui è attualmente installata l'applicazione. Se il percorso non è, riscrivere le voci del percorso in modo che puntino alla posizione corrente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di applicazioni COM](registering-com-applications.md)
</dt> </dl>

 

 




