---
description: Per ulteriori informazioni sul diagramma seguente, vedere la legenda del diagramma delle relazioni tra entità.
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: Gruppo di tabelle Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a5cc87e80c60505025825353272699db574bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968396"
---
# <a name="core-tables-group"></a>Gruppo di tabelle Core

Per ulteriori informazioni sul diagramma seguente, vedere la [legenda del diagramma delle relazioni tra entità](entity-relationship-diagram-legend.md).

![gruppo di tabelle Core](images/core.png)

Il gruppo principale è costituito da tabelle che descrivono le funzionalità e i componenti fondamentali dell'applicazione e del pacchetto di installazione. Gli sviluppatori di pacchetti di installazione dovrebbero quindi considerare come popolare queste tabelle prima perché l'organizzazione di gran parte del database diventerà evidente dal contenuto di questo gruppo.

-   La [tabella Feature](feature-table.md) elenca tutte le funzionalità appartenenti all'applicazione.
-   La [tabella della condizione](condition-table.md) contiene le espressioni condizionali che determinano se verrà installata una particolare funzionalità o meno.
-   Nella [tabella FeatureComponents](featurecomponents-table.md) vengono descritti i componenti appartenenti a ciascuna funzionalità.
-   La [tabella Component](component-table.md) elenca tutti i componenti appartenenti all'installazione.
-   Nella [tabella directory](directory-table.md) sono elencate le directory necessarie durante l'installazione. Poiché ogni componente deve essere associato a una sola directory, la tabella dei componenti è strettamente correlata a questa tabella e include una chiave esterna per la tabella di directory.
-   Nella [tabella PublishComponent](publishcomponent-table.md) sono elencate le funzionalità e i componenti pubblicati per l'utilizzo da parte di altre applicazioni. I [componenti e le funzionalità](components-and-features.md) sono i due tipi di annunci di funzionalità.
-   La [tabella MsiAssembly](msiassembly-table.md) specifica le impostazioni Windows Installer per gli assembly di Common Language Runtime di .NET Framework e Win32.
-   La [tabella MsiAssemblyName](msiassemblyname-table.md) specifica lo schema per gli elementi di un nome di assembly cache forte per un Common Language Runtime o un assembly Win32.
-   La [tabella ComPlus](complus-table.md) contiene le informazioni necessarie per installare le applicazioni com+.
-   La [tabella IsolatedComponent](isolatedcomponent-table.md) associa il componente specificato nella \_ colonna applicazione componente (in genere un file con estensione exe) con il componente specificato nella \_ colonna condivisa componente (in genere una DLL condivisa).
-   La [tabella di aggiornamento](upgrade-table.md) contiene le informazioni necessarie durante gli [aggiornamenti principali](major-upgrades.md).

 

 



