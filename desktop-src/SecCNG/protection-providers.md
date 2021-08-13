---
description: A partire Windows 8, Microsoft ha iniziato a distribuire i provider che consentono di condividere in modo sicuro segreti e messaggi crittografati tra computer.
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: Provider di protezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fe4c688eec734a7c32d1a85eaec2d9ebf132834a5970802cecb2639240e7d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907192"
---
# <a name="protection-providers"></a>Provider di protezione

A partire Windows 8, Microsoft ha iniziato a distribuire i provider che consentono di condividere in modo sicuro segreti e messaggi crittografati tra computer. Esistono attualmente due provider di protezione chiave. Il provider Microsoft Key Protection consente di proteggere il contenuto in un gruppo in una foresta Active Directory. Il provider Microsoft Client Key Protection consente di proteggere il contenuto in un set di credenziali Web.

La protezione corretta da usare viene scelta automaticamente quando la funzione [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) analizza la stringa della regola del descrittore di protezione specificata come input. Il provider Microsoft Key Protection viene scelto per le stringhe di regola che iniziano con SID, SDDL e LOCAL. Il provider Microsoft Client Key Protection analizza le stringhe delle regole che iniziano con WEBCREDENTIALS. Per altre informazioni sulle stringhe delle regole, vedere [Descrittori di protezione.](protection-descriptors.md)

> [!Note]  
> I provider personalizzati non sono attualmente consentiti. [DPAPI CNG](cng-dpapi.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[Descrittori di protezione](protection-descriptors.md)
</dt> </dl>

 

 



