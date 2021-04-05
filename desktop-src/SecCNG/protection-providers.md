---
description: A partire da Windows 8, Microsoft ha iniziato a distribuire i provider che consentono di condividere in modo sicuro i segreti e i messaggi crittografati tra i computer.
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: Provider di protezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c262fcfbfa5ab0842f103849af3d67b20f8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967186"
---
# <a name="protection-providers"></a>Provider di protezione

A partire da Windows 8, Microsoft ha iniziato a distribuire i provider che consentono di condividere in modo sicuro i segreti e i messaggi crittografati tra i computer. Attualmente sono disponibili due provider di protezione con chiave. Il provider Microsoft Key Protection consente di proteggere il contenuto di un gruppo in una foresta Active Directory. Il provider Microsoft client Key Protection consente di proteggere il contenuto di un set di credenziali Web.

La protezione corretta da usare viene scelta automaticamente quando la funzione [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) analizza la stringa della regola del descrittore di protezione fornita come input. Il provider Microsoft Key Protection viene scelto per le stringhe di regole che iniziano con SID, SDDL e LOCAL. Il provider Microsoft client Key Protection analizza le stringhe delle regole che iniziano con webcredentials. Per ulteriori informazioni sulle stringhe delle regole, vedere [descrittori di protezione](protection-descriptors.md).

> [!Note]  
> I provider personalizzati non sono attualmente consentiti. [DPAPI CNG](cng-dpapi.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DPAPI CNG](cng-dpapi.md)
</dt> <dt>

[**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[Descrittori di protezione](protection-descriptors.md)
</dt> </dl>

 

 



