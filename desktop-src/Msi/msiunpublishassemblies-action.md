---
description: L'azione MsiUnpublishAssemblies gestisce l'annuncio degli assembly Common Language Runtime e degli assembly Win32 da rimuovere.
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: Azione MsiUnpublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d398c66781e6e356b110828c56de6f5e616775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884113"
---
# <a name="msiunpublishassemblies-action"></a>Azione MsiUnpublishAssemblies

L'azione MsiUnpublishAssemblies gestisce l'annuncio degli assembly Common Language Runtime e degli assembly Win32 da rimuovere. L'azione esegue una query sulla [tabella MsiAssembly](msiassembly-table.md) per determinare quali assembly hanno annunciato o installato funzionalità da rimuovere dal Global assembly cache e quali assembly hanno un componente padre annunciato o installato rimosso da un percorso isolato per una particolare applicazione. Per informazioni, vedere [installazione di assembly nella global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) e [installazione di assembly Win32](installation-of-win32-assemblies.md).

Nei sistemi che eseguono Windows XP e versioni successive Windows Installer possibile installare assembly Win32 come [assembly side-by-side](side-by-side-assemblies.md). Per ulteriori informazioni, vedere [informazioni sulle applicazioni isolate e gli assembly affiancati](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione MsiUnpublishAssemblies deve essere successiva all' [azione InstallInitialize](installinitialize-action.md) nella [tabella InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | Contesto dell'applicazione.       |
| \[2\] | Nome dell'assembly.             |



 

## <a name="remarks"></a>Commenti

L' [azione MsiPublishAssemblies](msipublishassemblies-action.md) gestisce l'annuncio degli assembly da annunciare o installare.

 

 
