---
description: "Per annunciare un'applicazione in base all'installazione per utente quando l'applicazione richiede privilegi elevati (ovvero di sistema) per l'installazione, usare le linee guida riportate nell'elenco seguente:"
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: Annuncio di un'applicazione Per-User da installare con privilegi elevati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d9888714f28282e060b3a1e7eea0291b4e0e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311065"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a>Annuncio di un'applicazione Per-User da installare con privilegi elevati

Per annunciare un'applicazione in base all'installazione per utente quando l'applicazione richiede privilegi elevati (ovvero di sistema) per l'installazione, usare le linee guida riportate nell'elenco seguente:

-   Il processo deve essere un servizio eseguito con l'account di sistema LocalSystem in Windows XP o versione successiva.
-   Generare uno script di annuncio chiamando [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) o [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).
-   Il processo deve rappresentare l'utente che è la destinazione dell'annuncio.
-   Chiamare [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)e usare i \_ \| tasti di \_ \_ \| \_ \_ \| \_ scelta rapida SCRIPTFLAGS CACHEINFO SCRIPTFLAGS REGDATA appinfo SCRIPTFLAGS REGDATA CNFGINFO SCRIPTFLAGS.

Quando si seguono le linee guida, si annuncia un'applicazione a un utente specifico e quando l'utente sceglie di installare, l'applicazione viene installata con privilegi elevati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazione di patch Per-User applicazioni gestite](patching-per-user-managed-applications.md)
</dt> </dl>

 

 



