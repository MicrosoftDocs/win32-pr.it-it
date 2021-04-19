---
description: ICE22 utilizza la tabella FeatureComponents per convalidare il mapping delle funzionalità e dei componenti a cui viene fatto riferimento nella tabella PublishComponent.
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26574b11f9d908026d901a74632766998246d31a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314229"
---
# <a name="ice22"></a>ICE22

ICE22 utilizza la [tabella FeatureComponents](featurecomponents-table.md) per convalidare il mapping delle funzionalità e dei componenti a cui viene fatto riferimento nella [tabella PublishComponent](publishcomponent-table.md).

## <a name="result"></a>Risultato

ICE22 Invia un messaggio di errore se le funzionalità e i componenti non sono mappati correttamente nella [tabella PublishComponent](publishcomponent-table.md).

## <a name="example"></a>Esempio

Per l'esempio seguente ICE22 Invia un errore che non {00000003-0004-0000-0000-624474732465} dispone del mapping corretto per le colonne feature \_ e Component \_ .

[Tabella PublishComponent](publishcomponent-table.md) (parziale)



| ComponentId                            | Funzionalità\_ | Componente\_ |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | Feat1     | Comp1       |
| {00000003-0004-0000-0000-624474732465} | Feat1     | Comp2       |



 

[Tabella FeatureComponents](featurecomponents-table.md) (parziale)



| Funzionalità\_ | Componente\_ |
|-----------|-------------|
| Feat1     | Comp1       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



