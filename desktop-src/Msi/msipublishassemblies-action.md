---
description: L'azione MsiPublishAssemblies gestisce l'annuncio degli assembly Common Language Runtime e degli assembly Win32.
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: Azione MsiPublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24e1787aeb87cf00eb82aefab375771c7c1ddc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318655"
---
# <a name="msipublishassemblies-action"></a>Azione MsiPublishAssemblies

L'azione MsiPublishAssemblies gestisce l'annuncio degli assembly Common Language Runtime e degli assembly Win32. L'azione esegue una query sulla [tabella MsiAssembly](msiassembly-table.md) per determinare quali assembly hanno funzionalità annunciate o installate nel Global assembly cache e quali assembly dispongono di un componente padre annunciato o installato in un percorso isolato per una particolare applicazione. Per informazioni, vedere [installazione di assembly nella global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) e [installazione di assembly Win32](installation-of-win32-assemblies.md).

Nei sistemi Microsoft Windows XP e versioni successive Windows Installer possibile installare assembly Win32 come [assembly side-by-side](side-by-side-assemblies.md). Per ulteriori informazioni, vedere [informazioni sulle applicazioni isolate e gli assembly affiancati](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione MsiPublishAssemblies deve essere successiva all' [azione InstallInitialize](installinitialize-action.md) nella tabella [InstallExecuteSequence](installexecutesequence-table.md) o [AdvtExecuteSequence](advtexecutesequence-table.md).

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | Contesto dell'applicazione.       |
| \[2\] | Nome dell'assembly.             |



 

## <a name="remarks"></a>Commenti

Per ulteriori informazioni, vedere [assembly](assemblies.md).

L' [azione MsiUnpublishAssemblies](msiunpublishassemblies-action.md) gestisce l'annuncio degli assembly da rimuovere.

 

 
