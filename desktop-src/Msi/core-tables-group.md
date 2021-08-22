---
description: Per altre informazioni sul diagramma seguente, vedere legenda del diagramma delle relazioni di entità.
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: Gruppo tabelle principali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a8704a13e71f019e3d0686384057d3f209de06530c97bda6f0a63ff352d4db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948541"
---
# <a name="core-tables-group"></a>Gruppo tabelle principali

Per altre informazioni sul diagramma seguente, vedere legenda del diagramma [delle relazioni di entità.](entity-relationship-diagram-legend.md)

![gruppo di tabelle principali](images/core.png)

Il gruppo principale è costituito da tabelle che descrivono le funzionalità e i componenti fondamentali dell'applicazione e del pacchetto del programma di installazione. Gli sviluppatori di pacchetti di installazione devono quindi considerare come popolare prima queste tabelle perché l'organizzazione di gran parte del database diventerà evidente dal contenuto di questo gruppo.

-   La [tabella Funzionalità elenca](feature-table.md) tutte le funzionalità appartenenti all'applicazione.
-   La [tabella Condizione](condition-table.md) contiene le espressioni condizionali che determinano se una particolare funzionalità verrà installata o meno.
-   La [tabella FeatureComponents](featurecomponents-table.md) descrive i componenti che appartengono a ogni funzionalità.
-   Nella [tabella Componente sono](component-table.md) elencati tutti i componenti appartenenti all'installazione.
-   Nella [tabella Directory sono](directory-table.md) elencate le directory necessarie durante l'installazione. Poiché ogni componente deve essere associato a una sola directory, la tabella Component è strettamente correlata a questa tabella e ha una chiave esterna alla tabella Directory.
-   La [tabella PublishComponent](publishcomponent-table.md) elenca le funzionalità e i componenti pubblicati per l'uso da parte di altre applicazioni. [Componenti e funzionalità sono](components-and-features.md) i due tipi di annuncio di funzionalità.
-   La [tabella MsiAssembly](msiassembly-table.md) specifica le Windows del programma di installazione per .NET Framework assembly Common Language Runtime e win32.
-   La [tabella MsiAssemblyName](msiassemblyname-table.md) specifica lo schema per gli elementi di un nome di Assembly Cache sicuro per un assembly Common Language Runtime o Win32.
-   La [tabella Complus contiene](complus-table.md) le informazioni necessarie per installare le applicazioni COM+.
-   La [tabella IsolatedComponent](isolatedcomponent-table.md) associa il componente specificato nella colonna Applicazione componente (in genere un .exe) al componente specificato nella colonna Componente condiviso (in genere una \_ DLL \_ condivisa).
-   La [tabella Upgrade contiene](upgrade-table.md) le informazioni necessarie durante gli aggiornamenti [principali.](major-upgrades.md)

 

 



