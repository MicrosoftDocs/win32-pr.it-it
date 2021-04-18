---
description: Ogni funzionalità Windows Installer utilizza uno o più componenti di Windows Installer e le funzionalità possono condividere i componenti.
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: Specifica di relazioni Feature-Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05ff15f4c735ac7d081c16f49f1aafe555a96db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307837"
---
# <a name="specifying-feature-component-relationships"></a>Specifica di relazioni Feature-Component

Ogni [funzionalità Windows Installer](windows-installer-features.md) utilizza uno o più [componenti di Windows Installer](windows-installer-components.md)e le funzionalità possono condividere i componenti. La [tabella FeatureComponents](featurecomponents-table.md) definisce la relazione tra le funzionalità e i componenti. Vedere il [gruppo di tabelle](core-tables-group.md) e i [componenti e le funzionalità](components-and-features.md) principali nella Panoramica di Windows Installer. In questa sezione si aggiungono informazioni alla tabella FeatureComponents dell'esempio del blocco note.

Utilizzare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella FeatureComponents vuota.

[Tabella FeatureComponents](featurecomponents-table.md)



| Funzionalità\_ | Componente\_ |
|-----------|-------------|
| Baseball  | Baseball    |
| Concerto   | Concerto     |
| Danza     | Danza       |
| Calcio  | Calcio    |
| Help      | Help        |
| January   | January     |
| NewYears  | NewYears    |
| Blocco note   | Blocco note     |
| File Leggimi    | Blocco note     |



 

[Continua](adding-registry-information.md)

 

 



