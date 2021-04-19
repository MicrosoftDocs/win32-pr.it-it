---
description: L'azione PublishFeatures scrive lo stato di ogni funzionalità nel registro di sistema.
ms.assetid: 8205e865-e625-43b9-8ce9-cff8026b2717
title: Azione PublishFeatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5356ef89aa2651c470917a9b8d81b79ee83d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311729"
---
# <a name="publishfeatures-action"></a>Azione PublishFeatures

L'azione PublishFeatures scrive lo stato di ogni funzionalità nel registro di sistema. Lo stato della funzionalità può essere assente, pubblicizzato o installato. L'azione PublishFeatures scrive anche il mapping del componente della funzionalità nel registro di sistema per ogni funzionalità installata.

L'azione PublishFeatures esegue una query sulla tabella [FeatureComponents](featurecomponents-table.md), la [tabella delle funzionalità](feature-table.md)e la [tabella dei componenti](component-table.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione PublishFeatures deve essere precedente a [PublishProduct](publishproduct-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione        |
|-------|-----------------------------------|
| \[1\] | Identificatore della funzionalità annunciata. |



 

## <a name="remarks"></a>Commenti

L'azione PublishFeatures pubblica la composizione di tutte le funzionalità selezionate per l'annuncio o l'installazione.

 

 



