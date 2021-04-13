---
description: Il Windows Installer installa gli assembly Common Language Runtime nel Global Assembly Cache usando il Framework Microsoft .NET.
ms.assetid: 21d535d5-f05b-411a-8719-2662e6046fbd
title: Installazione degli assembly nella global assembly cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719be313ad74374950092936bbd6124da779a0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226491"
---
# <a name="installation-of-assemblies-to-the-global-assembly-cache"></a>Installazione degli assembly nella global assembly cache

Il Windows Installer installa gli assembly Common Language Runtime nel Global Assembly Cache usando il Framework Microsoft .NET. Quando si installano gli assembly nel Global Assembly Cache, il programma di installazione non può utilizzare la stessa struttura di directory e le stesse regole di versione del file utilizzata per l'installazione di componenti Windows Installer normali. I componenti di Windows Installer normali possono essere installati in più percorsi di directory da prodotti diversi. Gli assembly possono esistere solo una volta nel Assembly Cache. Ogni assembly viene aggiunto e rimosso dal Assembly Cache come intero indivisibile; Pertanto, tutti i file che includono un assembly vengono sempre installati o rimossi insieme.

Il costo del disco dei componenti di Windows Installer regolari e degli assembly Common Language Runtime viene calcolato in modo diverso. Il costo totale del disco di un componente Windows Installer regolare include i costi locali, i costi di origine e i costi di rimozione. Per informazioni dettagliate, vedere [costo dei file](file-costing.md). Questo metodo non può essere usato per il costo di Common Language Runtime assembly perché questi possono avere client diversi da Windows Installer. Il costo degli assembly di Common Language Runtime deve essere determinato eseguendo una query sulla Common Language Runtime di Microsoft .NET Framework.

Il Windows Installer utilizza un processo transazionale in due passaggi per installare i prodotti contenenti Common Language Runtime assembly. In questo modo è possibile eseguire il rollback dell'installazione e della rimozione degli assembly. Per ulteriori informazioni, vedere [rollback degli assembly nella global assembly cache](rollback-of-assemblies-in-the-global-assembly-cache.md).

Si noti che gli assembly installati nel Global Assembly Cache da un'installazione di nel contesto di [installazione](installation-context.md) per utente non sono protetti da protezione file di Windows. Gli assembly installati nel Global Assembly Cache da un'installazione nel contesto di installazione per computer sono protetti da [Protezione risorse di Windows](../wfp/windows-resource-protection-portal.md).

 

 
