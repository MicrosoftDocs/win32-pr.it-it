---
title: Nozioni di base su DRM
description: Nozioni di base su DRM
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- Windows Media Format SDK, nozioni di base su DRM
- digital rights management (DRM), informazioni
- DRM (digital rights management),about
- digital rights management (DRM), protezione del contenuto
- DRM (digital rights management), protezione del contenuto
- digital rights management (DRM), creazione di pacchetti di contenuto
- DRM (digital rights management), creazione di pacchetti di contenuto
- digital rights management (DRM), lettura di contenuto protetto
- DRM (digital rights management), lettura di contenuto protetto
- protezione del contenuto
- creazione di pacchetti di contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ef4439308868b0d77db1e9cefac7381fb8fd9ee78be50cccbf2a8dc26e4176
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086141"
---
# <a name="drm-basics"></a>Nozioni di base su DRM

Le Windows DRM multimediali sono piuttosto semplici dal punto di vista di Windows Media Format SDK. I componenti dell'SDK possono essere usati per proteggere il contenuto e riprodurre contenuto protetto.

## <a name="protecting-content"></a>Protezione del contenuto

La protezione del contenuto (detta anche contenuto di creazione pacchetti) comporta la crittografia della sezione dei dati del file e l'inclusione di alcune informazioni nell'intestazione del file che consentono ai lettori di decrittografare il contenuto.

Per crittografare il contenuto, è necessaria una chiave, ovvero un valore usato per eseguire il seeding degli algoritmi di crittografia. Una chiave è costituito da due parti: un valore di semi di chiave (o chiave privata) e un identificatore di chiave (o chiave pubblica). Il valore di seed della chiave è il valore segreto con cui si codifica il contenuto. L'identificatore di chiave è un valore pubblico incluso nell'intestazione di un file protetto.

Quando un file è protetto, non può essere decrittografato senza una licenza. Una licenza include informazioni che specificano le condizioni per l'utilizzo per il contenuto protetto. Le condizioni di una licenza vengono decidete dal proprietario del contenuto e possono essere personalizzate in base a un'ampia gamma di esigenze. Parte del processo di creazione del pacchetto di un file è includere l'URL di una pagina Web in cui gli utenti possono acquisire una licenza per accedere al contenuto.

## <a name="reading-protected-content"></a>Lettura di contenuto protetto

Per leggere il contenuto protetto, una licenza per il contenuto deve risiedere nel computer client. Alcune restrizioni di licenza vengono controllate internamente dai componenti DRM di Windows Media Format SDK, mentre altre devono essere applicate dall'applicazione.

È possibile usare gli oggetti di Windows Media Format SDK per aiutare l'utente ad acquisire licenze per il contenuto ed eseguire altre attività amministrative, ad esempio l'aggiornamento dei componenti DRM e il backup delle licenze.

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




