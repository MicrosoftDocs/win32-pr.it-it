---
title: Azioni e diritti
description: Azioni e diritti
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, licenze per DRM
- Digital Rights Management (DRM), azioni
- DRM (Digital Rights Management), azioni
- Digital Rights Management (DRM), diritti
- DRM (Digital Rights Management), diritti
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- licenze, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d044850bb5ee73e804065c67840362ec0b7b0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044182"
---
# <a name="actions-and-rights"></a>Azioni e diritti

Quando un file viene protetto con Windows Media DRM, l'utilizzo è completamente limitato. È possibile emettere licenze per consentire a un utente di usare il contenuto in modi specifici. Ogni modo in cui un utente può usare il contenuto è descritto da un'azione. Ad esempio, la riproduzione di un file in un computer è un'azione.

Una licenza che Abilita una determinata azione è detta concessione di un diritto. Ad esempio, una licenza può concedere il diritto di riprodurre il contenuto in un computer.

Le azioni e i diritti si riferiscono alle stesse modalità di utilizzo del contenuto. La differenza consiste nel fatto che l'azione fa riferimento all'uso, mentre il diritto fa riferimento all'autorizzazione. Nonostante questa distinzione, le parole Action e right vengono spesso usate in modo interscambiabile in questa documentazione e in altri documenti che descrivono Windows Media DRM.

Le azioni gestite da diritti DRM di Windows Media sono elencate nella sezione [costanti di diritti](rights-constants.md) di questa documentazione.

Alcuni metodi delle API estese del client Windows Media DRM utilizzano costanti diverse per fare riferimento ai diritti DRM di base. Ad esempio, il metodo [**IWMDRMLicenseQuery:: QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) usa un set di stringhe specifiche per gli Stati delle licenze. Anche se queste costanti definiscono stringhe diverse rispetto alle costanti Rights di base, fanno riferimento agli stessi diritti nella licenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](drmconcepts.md)
</dt> </dl>

 

 




