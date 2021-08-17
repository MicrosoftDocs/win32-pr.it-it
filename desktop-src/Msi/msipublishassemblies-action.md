---
description: L'azione MsiPublishAssemblies gestisce l'annuncio di assembly Common Language Runtime e assembly Win32.
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: Azione MsiPublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524175a957249a48f7c72409ad7b4c55b31f642753db11875a9567ef35a2acf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804191"
---
# <a name="msipublishassemblies-action"></a>Azione MsiPublishAssemblies

L'azione MsiPublishAssemblies gestisce l'annuncio di assembly Common Language Runtime e assembly Win32. L'azione esegue una query sulla tabella [MsiAssembly](msiassembly-table.md) per determinare quali assembly hanno funzionalità annunciate o installate nella Global Assembly Cache e quali assembly hanno un componente padre annunciato o installato in un percorso isolato per una determinata applicazione. Per informazioni, vedere [Installazione di assembly nella Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) e Installazione di assembly [Win32](installation-of-win32-assemblies.md).

Nei sistemi Microsoft Windows XP e versioni successive, Windows Installer può installare assembly Win32 come [assembly side-by-side.](side-by-side-assemblies.md) Per altre informazioni, vedere Informazioni sulle applicazioni isolate e sugli [assembly side-by-side.](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md)

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione MsiPublishAssemblies deve essere eseguita dopo l'azione [InstallInitialize](installinitialize-action.md) nella tabella [InstallExecuteSequence](installexecutesequence-table.md) o [nella tabella AdvtExecuteSequence](advtexecutesequence-table.md).

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | Contesto dell'applicazione.       |
| \[2\] | Nome dell'assembly.             |



 

## <a name="remarks"></a>Commenti

Per altre informazioni, vedere [Assembly](assemblies.md).

[L'azione MsiUnpublishAssemblies](msiunpublishassemblies-action.md) gestisce l'annuncio degli assembly rimossi.

 

 
