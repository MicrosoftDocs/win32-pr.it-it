---
description: "Per annunciare un'applicazione in base all'installazione per utente quando l'applicazione richiede privilegi elevati (ovvero di sistema) per l'installazione, usare le linee guida nell'elenco seguente:"
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: Annuncio di Per-User'applicazione da installare con privilegi elevati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdced246f90a345b5b2cc599541119a26e29e4d9a1d708be1ee8299d55d3c28d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082961"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a>Annuncio di Per-User'applicazione da installare con privilegi elevati

Per annunciare un'applicazione in base all'installazione per utente quando l'applicazione richiede privilegi elevati (ovvero di sistema) per l'installazione, usare le linee guida nell'elenco seguente:

-   Il processo deve essere un servizio eseguito con l'account di sistema LocalSystem Windows XP o versioni successive.
-   Generare uno script di annuncio chiamando [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) o [**MsiAdvertiseProductEx.**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)
-   Il processo deve rappresentare l'utente di destinazione dell'annuncio.
-   Chiamare [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)e usare i flag SCRIPTFLAGS \_ CACHEINFO \| SCRIPTFLAGS \_ REGDATA \_ APPINFO \| SCRIPTFLAGS \_ REGDATA \_ CNFGINFO \| SCRIPTFLAGS \_ SHORTCUTS.

Quando si seguono le linee guida, si annuncia un'applicazione a un utente specifico e quando l'utente sceglie di installarlo, l'applicazione viene installata con privilegi elevati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazione di Per-User applicazioni gestite](patching-per-user-managed-applications.md)
</dt> </dl>

 

 



