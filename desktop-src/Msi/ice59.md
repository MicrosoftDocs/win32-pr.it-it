---
description: ICE59 verifica che i collegamenti annunciati appartengano ai componenti installati dalla funzionalità di destinazione del collegamento.
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1a8d6318a9b4525941edd3873c9fc35bd11f488e42c8a82da71c4b2c0b9b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044021"
---
# <a name="ice59"></a>ICE59

ICE59 verifica che i collegamenti annunciati appartengano ai componenti installati dalla funzionalità di destinazione del collegamento.

Gli errori segnalati da ICE59 in genere comportano il comportamento seguente:

1.  Il collegamento annunciato avvierà il Windows installer per installare la funzionalità elencata nella colonna Destinazione.
2.  Tuttavia, poiché la [tabella FeatureComponents](featurecomponents-table.md) non esegue il mapping della funzionalità di destinazione al componente contenente il collegamento, il keyfile del componente (attivato dal collegamento) non viene installato.
3.  Di conseguenza, il collegamento viene interrotto e non verrà fatto nulla.

## <a name="result"></a>Risultato

ICE59 invia un errore se un collegamento annunciato non appartiene ai componenti installati dalla funzionalità di destinazione del collegamento.

## <a name="example"></a>Esempio

ICE59 segnala l'errore seguente per l'esempio illustrato:

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

In questo caso, ShortcutB annuncia FeatureA e, se attivato, avvia il file di chiave di ComponentB. Tuttavia, ComponentB non viene mai installato da FeatureA, quindi anche al termine della fase di installazione su richiesta, la destinazione del collegamento non esiste.

Per correggere l'errore, aggiungere una riga alla [tabella FeatureComponents](featurecomponents-table.md) che associa FeatureA e ComponentB.

[Tabella dei collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Destinazione   | Componente\_ |
|-----------|----------|-------------|
| CollegamentoB | FunzionalitàA | ComponenteB  |



 

[Tabella FeatureComponents](featurecomponents-table.md)



| Funzionalità\_ | Componente\_ |
|-----------|-------------|
| FunzionalitàA  | Componenta  |



 

[Tabella delle funzionalità](feature-table.md) (parziale)



| Funzionalità  | Level |
|----------|-------|
| FunzionalitàA | 10    |



 

[Tabella dei componenti](component-table.md) (parziale)



| Componente  | KeyPath |
|------------|---------|
| Componenta | FileA   |
| ComponenteB | FileB   |



 

[Tabella file](file-table.md) (parziale)



| File  | Componente\_ | Sequenza |
|-------|-------------|----------|
| FileA | Componenta  | 1        |
| FileB | ComponenteB  | 2        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



