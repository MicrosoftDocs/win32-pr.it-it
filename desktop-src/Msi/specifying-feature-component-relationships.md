---
description: Ogni Windows programma di installazione usa uno o più componenti Windows programma di installazione e le funzionalità possono condividere i componenti.
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: Specifica di Feature-Component relazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1d7a79e35822d5a0ad67f43297ec461eb3c2fd766c946cc414a571c148de5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627871"
---
# <a name="specifying-feature-component-relationships"></a>Specifica di Feature-Component relazioni

Ogni [Windows programma di installazione usa](windows-installer-features.md) uno o più componenti Windows [programma](windows-installer-components.md)di installazione e le funzionalità possono condividere i componenti. La [tabella FeatureComponents](featurecomponents-table.md) definisce la relazione tra funzionalità e componenti. Vedere il [gruppo e i componenti](core-tables-group.md) e le funzionalità [delle](components-and-features.md) tabelle principali nella panoramica Windows programma di installazione. In questa sezione si aggiungono informazioni alla tabella FeatureComponents dell'Blocco note esempio.

Usare l'editor di database per MNP2000.msi e immettere i dati seguenti nella tabella FeatureComponents vuota.

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

 

 



