---
title: Elenchi di autorizzazione e inclusione espliciti
description: Elenchi di autorizzazione e inclusione espliciti
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- Windows MEDIA Format SDK, esportazione DRM
- Windows Media Format SDK, esportazione
- Windows MEDIA Format SDK, elenchi espliciti di autorizzazioni e inclusione
- Windows MEDIA Format SDK, elenchi di autorizzazioni
- Windows MEDIA Format SDK, elenchi di inclusione
- digital rights management (DRM), esportazione
- DRM (Digital Rights Management),esportazione
- DRM (Digital Rights Management), elenchi espliciti di autorizzazione e inclusione
- DRM (Digital Rights Management),elenchi espliciti di autorizzazione e inclusione
- digital rights management (DRM), elenchi di autorizzazioni
- DRM (Digital Rights Management),elenchi di autorizzazioni
- digital rights management (DRM), elenchi di inclusione
- DRM (Digital Rights Management),elenchi di inclusione
- API estese del client DRM, elenchi espliciti di autorizzazione e inclusione
- API client estese, elenchi di autorizzazione e inclusione espliciti
- API estese del client DRM, elenchi di autorizzazioni
- API client estese, elenchi di autorizzazioni
- API estese del client DRM, elenchi di inclusione
- API client estese, elenchi di inclusione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee489d91002cacf7d8a0c89ffeef1752cd844aa089fabbe636e5e50fc185a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089731"
---
# <a name="explicit-authorization-and-inclusion-lists"></a>Elenchi di autorizzazione e inclusione espliciti

Le licenze possono contenere un elenco di inclusione per autorizzare in modo esplicito l'esportazione di contenuto protetto da Windows Media DRM ad altri schemi di protezione del contenuto (CPS). In base alle condizioni del contratto di licenza immesse con Microsoft per abilitare l'esportazione DRM, è possibile esportare solo in un CPS valido identificato nell'elenco di inclusione di una licenza.

Un elenco di inclusione è una matrice delimitata di identificatori univoci globali (GUID) ognuno dei quali rappresenta un CPS autorizzato specifico in cui è possibile esportare il contenuto. I GUID elencati in un elenco di inclusione sono indipendenti dai livelli di protezione dell'output (OPL) e dai livelli di protezione del contenuto (CPL). L'applicazione di queste restrizioni è responsabilità dell'applicazione.

> [!Note]  
> Quando si esegue Windows'esportazione di Media DRM su contenuto compresso, si accede all'elenco di inclusione tramite il [**metodo IWMDRMLicense::GetInclusionList.**](iwmdrmlicense-getinclusionlist.md) Quando si Windows l'esportazione di Media DRM su contenuto non compresso, usare il [**metodo IWMDRMReader3::GetInclusionList.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist)

 

Per registrare un nuovo sistema di protezione del contenuto come Windows'esportazione consentita di Media DRM nelle regole di conformità dell'esportazione di Windows Media DRM, contattare wmla@microsoft.com .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esportazione DRM**](drm-export.md)
</dt> </dl>

 

 




