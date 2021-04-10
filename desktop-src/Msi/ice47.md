---
description: ICE47 controlla la funzionalità e le tabelle FeatureComponents per le funzionalità con 1600 o più componenti.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa04c2df52571f56612242d2dc7da8b5a91647c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227406"
---
# <a name="ice47"></a>ICE47

ICE47 controlla la [funzionalità](feature-table.md) e le tabelle [FeatureComponents](featurecomponents-table.md) per le funzionalità con 1600 o più componenti.

## <a name="result"></a>Risultato

ICE47 Invia un messaggio di errore se una funzionalità supera il limite massimo di 1600 componenti per funzionalità.

## <a name="example"></a>Esempio

ICE47 segnala l'avviso seguente:

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

[Tabella delle funzionalità](feature-table.md) (parziale)



| Funzionalità  |
|----------|
| Feature1 |



 

[Tabella FeatureComponents](featurecomponents-table.md) (parziale)



| Azione   | Condizione     |
|----------|---------------|
| Feature1 | Component1    |
| Feature1 | Component1600 |



 

Per correggere il problema, provare a suddividere la funzionalità in diverse funzionalità

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



