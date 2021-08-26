---
title: Azioni e diritti
description: Azioni e diritti
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, licenze per DRM
- digital rights management (DRM), azioni
- DRM (Digital Rights Management),azioni
- digital rights management (DRM),rights
- DRM (Digital Rights Management),diritti
- digital rights management (DRM), licenze
- DRM (Digital Rights Management),licenze
- licenze, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b822c0350af12c5e266570a031ca0d3eda7c99b4b8451b751786a60a4a0908d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089771"
---
# <a name="actions-and-rights"></a>Azioni e diritti

Quando un file è protetto tramite Windows Media DRM, l'uso di questo file è completamente limitato. Le licenze possono essere rilasciate per consentire a un utente di usare il contenuto in modi specifici. Ogni modo in cui un utente può usare il contenuto è descritto da un'azione. Ad esempio, la riproduzione di un file in un computer è un'azione.

Si dice che una licenza che consente una determinata azione concede un diritto. Ad esempio, una licenza può concedere il diritto di riprodurre contenuto in un computer.

Le azioni e i diritti si riferiscono agli stessi modi di usare il contenuto. La differenza è che l'azione fa riferimento all'uso mentre il diritto fa riferimento all'autorizzazione. Nonostante questa distinzione, le parole action e right vengono spesso usate in modo intercambiabile in questa documentazione e in altri documenti che descrivono Windows Media DRM.

Le azioni regolate dai Windows media DRM sono elencate nella sezione [Rights Constants](rights-constants.md) di questa documentazione.

Alcuni metodi delle API Windows client DRM multimediale usano costanti diverse per fare riferimento ai diritti DRM di base. Ad esempio, il [**metodo IWMDRMLicenseQuery::QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) usa un set di stringhe specifiche per gli stati di licenza. Anche se queste costanti definiscono stringhe diverse rispetto alle costanti dei diritti di base, fanno riferimento agli stessi diritti nella licenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](drmconcepts.md)
</dt> </dl>

 

 




