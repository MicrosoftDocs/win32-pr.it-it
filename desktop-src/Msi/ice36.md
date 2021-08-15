---
description: ICE36 verifica che ogni icona nella tabella Icon sia elencata almeno una volta nella proprietà ARPPRODUCTICON o nelle tabelle Class, ProgId o Shortcut.
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c3d951e90ac9f3dc46a564757c1a1d5a1737bf054740e3109a26c8c7b91055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635304"
---
# <a name="ice36"></a>ICE36

ICE36 verifica che ogni icona nella tabella Icon sia elencata almeno una volta nella proprietà [**ARPPRODUCTICON**](arpproducticon.md) o nelle tabelle [Class](class-table.md), [ProgId](progid-table.md) [o Shortcut.](shortcut-table.md)

Durante l'annuncio, il programma di installazione installa tutte le icone elencate nella [tabella Icona](icon-table.md) nel computer dell'utente. La presenza di icone inutilizzate nella tabella Icon non impedisce l'esecuzione dell'installazione, ma aumenta inutilmente le dimensioni del file .msi e il tempo e lo spazio necessari per annunciare una funzionalità.

Se non viene fatto riferimento a un'icona nella proprietà o nella tabella e non è disponibile alcuna interfaccia utente per creare un riferimento in fase di esecuzione, è necessario rimuovere l'icona per ottenere prestazioni migliori.

## <a name="result"></a>Risultato

ICE36 pubblica un messaggio se nella tabella Icon è presente un'icona a cui non viene fatto riferimento nelle tabelle [Class](class-table.md), [ProgId](progid-table.md)o [Shortcut](shortcut-table.md) e se non è disponibile alcuna interfaccia utente per creare tale riferimento in fase di esecuzione.

## <a name="example"></a>Esempio

ICE36 segnala l'errore seguente per l'esempio illustrato.

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

[Tabella delle icone](icon-table.md) (parziale)



| Nome  | Dati     |
|-------|----------|
| Icona1 | Control1 |
| Icona2 | Controllo2 |
| Icona3 | Controllo3 |
| Icona4 | Controllo4 |



 

[Tabella ProgID](progid-table.md) (parziale)



| ProgID    |
|-----------|
| Property1 |



 

[Tabella di classi](class-table.md) (parziale)



| CLSID                                  |
|----------------------------------------|
| {3E469ABA-3644-11d2-8892-00A0C981B015} |



 

[Tabella dei collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Icona\_ |
|-----------|--------|
| Collegamento1 | Icona2  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



