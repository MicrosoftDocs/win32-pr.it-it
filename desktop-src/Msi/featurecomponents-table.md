---
description: La tabella FeatureComponents definisce la relazione tra funzionalità e componenti. Per ogni funzionalità, in questa tabella sono elencati tutti i componenti che la costituiscono.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: Tabella FeatureComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7635a43784ee7e8fbb71c7161bb07d39ffe5238177ea2a7cdaabdeb18dc41e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430871"
---
# <a name="featurecomponents-table"></a>Tabella FeatureComponents

La tabella FeatureComponents definisce la relazione tra funzionalità e componenti. Per ogni funzionalità, in questa tabella sono elencati tutti i componenti che la costituiscono.

La tabella FeatureComponents include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Funzionalità\_   | [Identificatore](identifier.md) | S   | N        |
| Componente\_ | [Identificatore](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella [Feature](feature-table.md).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella [Component](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

È previsto un limite massimo di 1600 componenti per funzionalità.

I componenti possono essere condivisi da due o più funzionalità, vale a dire che lo stesso componente può essere indicato da più di una funzionalità.

A questa tabella viene fatto riferimento quando viene [eseguita l'azione PublishFeatures](publishfeatures-action.md) o [UnpublishFeatures.](unpublishfeatures-action.md)

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

 

 



