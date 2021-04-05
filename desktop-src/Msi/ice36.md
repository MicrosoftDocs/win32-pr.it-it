---
description: ICE36 verifica che ogni icona nella tabella delle icone sia elencata almeno una volta nella proprietà ARPPRODUCTICON o nelle tabelle di classe, ProgId o collegamento.
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f24eebc1b591edde418c59b6765d7ee91a00dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057808"
---
# <a name="ice36"></a>ICE36

ICE36 verifica che ogni icona nella tabella delle icone sia elencata almeno una volta nella proprietà [**arpproducticon**](arpproducticon.md) o nelle tabelle di [classe](class-table.md), [ProgID](progid-table.md)o [collegamento](shortcut-table.md) .

Durante l'annuncio, il programma di installazione installa tutte le icone elencate nella [tabella](icon-table.md) delle icone nel computer dell'utente. La presenza di icone inutilizzate nella tabella delle icone non impedisce l'esecuzione dell'installazione. Tuttavia, aumenta inutilmente le dimensioni del file con estensione msi e il tempo e lo spazio necessari per annunciare una funzionalità.

Se non viene fatto riferimento a un'icona nella proprietà o nella tabella e non è disponibile alcuna interfaccia utente per creare un riferimento in fase di esecuzione, è necessario rimuovere l'icona per ottenere prestazioni migliori.

## <a name="result"></a>Risultato

ICE36 Invia un messaggio se è presente un'icona nella tabella delle icone a cui non viene fatto riferimento nelle tabelle [class](class-table.md), [ProgID](progid-table.md)o [Shortcut](shortcut-table.md) e se non è disponibile alcuna interfaccia utente per creare un riferimento di questo tipo in fase di esecuzione.

## <a name="example"></a>Esempio

ICE36 segnala l'errore seguente per l'esempio illustrato.

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

[Tabella icone](icon-table.md) (parziale)



| Nome  | Data     |
|-------|----------|
| Icon1 | Control1 |
| Icon2 | Controllo2 |
| Icon3 | Control3 |
| Icon4 | Control4 |



 

[Tabella ProgId](progid-table.md) (parziale)



| ProgID    |
|-----------|
| Property1 |



 

[Tabella classi](class-table.md) (parziale)



| CLSID                                  |
|----------------------------------------|
| {3E469ABA-3644-11d2-8892-00A0C981B015} |



 

[Tabella collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Icona\_ |
|-----------|--------|
| Shortcut1 | Icon2  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



