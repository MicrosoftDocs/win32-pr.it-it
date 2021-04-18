---
description: ICE59 verifica che i collegamenti annunciati appartengano ai componenti installati dalla funzionalità di destinazione del collegamento.
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5631b723a158bb371fff3211654a70d694b6cb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310978"
---
# <a name="ice59"></a>ICE59

ICE59 verifica che i collegamenti annunciati appartengano ai componenti installati dalla funzionalità di destinazione del collegamento.

Gli errori segnalati da ICE59 in genere comportano il comportamento seguente:

1.  Il collegamento annunciato avvierà il Windows Installer per installare la funzionalità elencata nella colonna destinazione.
2.  Tuttavia, poiché la [tabella FeatureComponents](featurecomponents-table.md) non esegue il mapping della funzionalità di destinazione al componente contenente il collegamento, il file di base del componente (attivato dal collegamento) non è installato.
3.  Pertanto, il collegamento viene rotto e non eseguirà alcuna operazione.

## <a name="result"></a>Risultato

ICE59 Invia un errore se un collegamento annunciato non appartiene ai componenti installati dalla funzionalità di destinazione del collegamento.

## <a name="example"></a>Esempio

ICE59 segnala l'errore seguente per l'esempio illustrato:

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

In questo caso, ShortcutB annuncia FeatureA e, quando attivato, avvia il file di chiave di ComponentB. Tuttavia, ComponentB non viene mai installato da FeatureA, quindi anche dopo che la fase di installazione su richiesta è stata completata, la destinazione del collegamento non esiste.

Per correggere l'errore, aggiungere una riga alla [tabella FeatureComponents](featurecomponents-table.md) che associa FeatureA e ComponentB.

[Tabella collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Destinazione   | Componente\_ |
|-----------|----------|-------------|
| ShortcutB | FunzionalitàA | ComponentB  |



 

[Tabella FeatureComponents](featurecomponents-table.md)



| Funzionalità\_ | Componente\_ |
|-----------|-------------|
| FunzionalitàA  | ComponentA  |



 

[Tabella delle funzionalità](feature-table.md) (parziale)



| Funzionalità  | Level |
|----------|-------|
| FunzionalitàA | 10    |



 

[Tabella componenti](component-table.md) (parziale)



| Componente  | KeyPath |
|------------|---------|
| ComponentA | FileA   |
| ComponentB | FileB   |



 

[Tabella file](file-table.md) (parziale)



| File  | Componente\_ | Sequenza |
|-------|-------------|----------|
| FileA | ComponentA  | 1        |
| FileB | ComponentB  | 2        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



