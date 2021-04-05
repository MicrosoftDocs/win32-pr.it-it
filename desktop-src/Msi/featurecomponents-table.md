---
description: La tabella FeatureComponents definisce la relazione tra le funzionalità e i componenti. Per ogni funzionalità, in questa tabella sono elencati tutti i componenti che costituiscono tale funzionalità.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: Tabella FeatureComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c93a7c020f179843916b063b48e2e4d19f7bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754226"
---
# <a name="featurecomponents-table"></a>Tabella FeatureComponents

La tabella FeatureComponents definisce la relazione tra le funzionalità e i componenti. Per ogni funzionalità, in questa tabella sono elencati tutti i componenti che costituiscono tale funzionalità.

La tabella FeatureComponents include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Funzionalità\_   | [Identificatore](identifier.md) | S   | N        |
| Componente\_ | [Identificatore](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella](feature-table.md)delle funzionalità.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella dei componenti](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

È previsto un limite massimo di 1600 componenti per funzionalità.

I componenti possono essere condivisi da due o più funzionalità, ovvero lo stesso componente può essere definito da più di una funzionalità.

Questa tabella viene definita quando viene eseguita l'azione [PublishFeatures](publishfeatures-action.md) o [UnpublishFeatures](unpublishfeatures-action.md) .

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE21](ice21.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE47](ice47.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE69](ice69.md)  
</dl>

 

 



