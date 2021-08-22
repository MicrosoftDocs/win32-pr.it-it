---
description: ICE47 controlla le tabelle Feature e FeatureComponents per le funzionalità con 1600 o più componenti.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdcf1f71af9bb8784c15b159836d329a94e7e6f33b34c31cbba72f9b31349a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381951"
---
# <a name="ice47"></a>ICE47

ICE47 controlla le [tabelle Feature](feature-table.md) e [FeatureComponents](featurecomponents-table.md) per le funzionalità con 1600 o più componenti.

## <a name="result"></a>Risultato

ICE47 invia un messaggio di errore se una funzionalità supera il limite massimo di 1600 componenti per ogni funzionalità.

## <a name="example"></a>Esempio

ICE47 segnalerebbe l'avviso seguente:

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

[Tabella delle funzionalità](feature-table.md) (parziale)



| Funzionalità  |
|----------|
| Funzionalità1 |



 

[Tabella FeatureComponents](featurecomponents-table.md) (parziale)



| Azione   | Condition     |
|----------|---------------|
| Funzionalità1 | Componente1    |
| Funzionalità1 | Componente1600 |



 

Per correggere questo avviso, provare a suddividere la funzionalità in diverse funzionalità

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



