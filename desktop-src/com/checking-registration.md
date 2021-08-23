---
title: Controllo della registrazione
description: Controllo della registrazione
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7d7f03f1d76b780b49bec5d744a02beca9a3dc45417bf8c6efddd8ff5a9e9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501651"
---
# <a name="checking-registration"></a>Controllo della registrazione

Ogni volta che un'applicazione viene caricata, deve controllare la registrazione per determinare quanto segue:

-   Indica se i CLSID sono presenti nel Registro di sistema. Se non sono presenti, l'applicazione deve registrarsi come configurazione originale.
-   Indica se i CLSID dell'applicazione sono presenti nel registro ma non dispongono di informazioni correlate a OLE 2. In questo caso, l'applicazione deve eseguire la registrazione come configurazione originale.
-   Indica se il percorso contenente le voci del server ([LocalServer](localserver.md) e [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) e [InprocServer32](inprocserver32.md)e [DefaultIcon](defaulticon.md)) punta al percorso in cui è attualmente installata l'applicazione. In caso contrario, riscrivere le voci del percorso in modo che puntino alla posizione corrente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di applicazioni COM](registering-com-applications.md)
</dt> </dl>

 

 




