---
description: ICE22 usa la tabella FeatureComponents per convalidare il mapping di funzionalità e componenti a cui viene fatto riferimento nella tabella PublishComponent.
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 177fcef5441e5b82738c76face70427cc6865ae59c11542fca080b3dc521c5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529021"
---
# <a name="ice22"></a>ICE22

ICE22 usa la [tabella FeatureComponents per](featurecomponents-table.md) convalidare il mapping delle funzionalità e dei componenti a cui si fa riferimento nella [tabella PublishComponent](publishcomponent-table.md).

## <a name="result"></a>Risultato

ICE22 invia un messaggio di errore se le funzionalità e i componenti sono mappati in modo non corretto nella [tabella PublishComponent](publishcomponent-table.md).

## <a name="example"></a>Esempio

Nell'esempio seguente ICE22 registra un errore che {00000003-0004-0000-0000-624474732465} non ha il mapping corretto per le colonne Feature e \_ \_ Component.

[Tabella PublishComponent](publishcomponent-table.md) (parziale)



| Componentid                            | Funzionalità\_ | Componente\_ |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | Feat1     | Comp1       |
| {00000003-0004-0000-0000-624474732465} | Feat1     | Comp2       |



 

[Tabella FeatureComponents](featurecomponents-table.md) (parziale)



| Funzionalità\_ | Componente\_ |
|-----------|-------------|
| Feat1     | Comp1       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



