---
description: Il Windows installer installa gli assembly di Common Language Runtime nella Global Assembly Cache usando Microsoft .NET Framework.
ms.assetid: 21d535d5-f05b-411a-8719-2662e6046fbd
title: Installazione di assembly nella Global Assembly Cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dec84b507491da5b3ec4b2352044dc899230b41f41d2c81a943fba83b3ba0b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634209"
---
# <a name="installation-of-assemblies-to-the-global-assembly-cache"></a>Installazione di assembly nella Global Assembly Cache

Il Windows installer installa gli assembly di Common Language Runtime nella Global Assembly Cache usando Microsoft .NET Framework. Quando si installano assembly nella Global Assembly Cache, il programma di installazione non può usare la stessa struttura di directory e le stesse regole di versione dei file usate durante l'installazione dei normali componenti Windows Installer. I Windows programma di installazione possono essere installati in più percorsi di directory da prodotti diversi. Gli assembly possono esistere una sola volta nell'Assembly Cache. Ogni assembly viene aggiunto e rimosso dall'Assembly Cache come intero indivisibile. Pertanto, tutti i file che comprendono un assembly vengono sempre installati o rimossi insieme.

Il costo del disco dei componenti Windows installer e degli assembly di Common Language Runtime viene calcolato in modo diverso. Il costo totale del disco di un componente Windows installer standard include i costi locali, i costi di origine e i costi di rimozione. Per informazioni dettagliate, vedere [Determinazione dei costi dei file.](file-costing.md) Questo metodo non può essere usato per costare gli assembly di Common Language Runtime perché possono avere client diversi dal Windows installer. Il costo degli assembly di Common Language Runtime deve essere determinato tramite l'esecuzione di query in Microsoft .NET Framework Common Language Runtime.

Il Windows installer usa un processo transazionale in due passaggi per installare prodotti contenenti assembly Common Language Runtime. Ciò consente il rollback dell'installazione e della rimozione di assembly. Per altre informazioni, vedere [Rollback degli assembly nella Global Assembly Cache.](rollback-of-assemblies-in-the-global-assembly-cache.md)

Si noti che gli assembly installati nella Global Assembly [](installation-context.md) Cache da un'installazione nel contesto di installazione per utente non sono protetti Windows Protezione file. Gli assembly installati nella Global Assembly Cache da un'installazione nel contesto di installazione per computer sono protetti Windows [Resource Protection.](../wfp/windows-resource-protection-portal.md)

 

 
