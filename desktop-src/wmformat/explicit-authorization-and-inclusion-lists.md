---
title: Elenchi di inclusione e autorizzazione esplicita
description: Elenchi di inclusione e autorizzazione esplicita
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- Windows Media Format SDK, esportazione DRM
- Windows Media Format SDK, esportazione
- Windows Media Format SDK, elenco di autorizzazioni esplicite e di inclusione
- Windows Media Format SDK, elenchi di autorizzazione
- Windows Media Format SDK, elenchi di inclusione
- Digital Rights Management (DRM), esportazione
- DRM (Digital Rights Management), esportazione
- Digital Rights Management (DRM), esplicito autorizzazione e inclusione elenchi
- DRM (Digital Rights Management), autorizzazione esplicita e elenchi di inclusione
- Digital Rights Management (DRM), elenchi di autorizzazioni
- DRM (Digital Rights Management), elenchi di autorizzazioni
- Digital Rights Management (DRM), elenchi di inclusione
- DRM (Digital Rights Management), elenchi di inclusione
- API estese del client DRM, elenchi di autorizzazioni esplicite e di inclusione
- API estese client, elenco di autorizzazioni esplicite e di inclusione
- API estese del client DRM, elenchi di autorizzazioni
- API estese client, elenchi di autorizzazioni
- API estese del client DRM, elenchi di inclusione
- API estese client, elenchi di inclusione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2309bed28ffd3add2a75c1cd90488b9ef454659b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398558"
---
# <a name="explicit-authorization-and-inclusion-lists"></a>Elenchi di inclusione e autorizzazione esplicita

Le licenze possono contenere un elenco di inclusione per autorizzare in modo esplicito l'esportazione di contenuto protetto da DRM di Windows Media ad altri schemi di protezione del contenuto (CPS). In base ai termini del contratto di licenza stipulato con Microsoft per abilitare l'esportazione DRM, è possibile esportare solo in un CPS valido identificato nell'elenco di inclusione di una licenza.

Un elenco di inclusione è una matrice limitata di identificatori univoci globali (GUID) che ognuno rappresenta un CPS autorizzato specifico in cui il contenuto può essere esportato. I GUID elencati in un elenco di inclusione sono indipendenti dai livelli di protezione dell'output (OPL) e dai livelli di protezione del contenuto (CPL). Applicare queste restrizioni è responsabilità dell'applicazione.

> [!Note]  
> Quando si esegue l'esportazione DRM di Windows Media sui contenuti compressi, è possibile accedere all'elenco di inclusione tramite il metodo [**IWMDRMLicense:: Getinclusivion**](iwmdrmlicense-getinclusionlist.md) . Quando si esegue l'esportazione DRM di Windows Media su contenuto non compresso, usare il metodo [**IWMDRMReader3:: Getinclusive**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) .

 

Per registrare un nuovo sistema di protezione del contenuto come Windows Media DRM Export consentito nelle regole di conformità per l'esportazione di Windows Media DRM, contattare wmla@microsoft.com .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esportazione DRM**](drm-export.md)
</dt> </dl>

 

 




