---
description: L'azione MsiUnpublishAssemblies gestisce l'annuncio degli assembly Common Language Runtime e degli assembly Win32 che vengono rimossi.
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: Azione MsiUnpublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f640338e13f53b115ca3b93aa2a63987efb5aa7cf053d4c8a59d8d20d0f7e3fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943898"
---
# <a name="msiunpublishassemblies-action"></a>Azione MsiUnpublishAssemblies

L'azione MsiUnpublishAssemblies gestisce l'annuncio degli assembly Common Language Runtime e degli assembly Win32 che vengono rimossi. L'azione esegue una query sulla tabella [MsiAssembly](msiassembly-table.md) per determinare quali assembly hanno annunciato o installato funzionalità rimosse dalla Global Assembly Cache e quali assembly hanno un componente padre annunciato o installato che viene rimosso da un percorso isolato per una determinata applicazione. Per informazioni, vedere [Installazione di assembly nella Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) e Installazione di assembly [Win32](installation-of-win32-assemblies.md).

Nei sistemi che eseguono Windows XP e versioni successive, Windows installer può installare assembly Win32 come [assembly side-by-side.](side-by-side-assemblies.md) Per altre informazioni, vedere Informazioni sulle applicazioni isolate e sugli [assembly side-by-side.](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md)

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione MsiUnpublishAssemblies deve essere eseguita dopo [l'azione InstallInitialize](installinitialize-action.md) nella [tabella InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | Contesto dell'applicazione.       |
| \[2\] | Nome dell'assembly.             |



 

## <a name="remarks"></a>Commenti

[L'azione MsiPublishAssemblies](msipublishassemblies-action.md) gestisce l'annuncio degli assembly annunciati o installati.

 

 
