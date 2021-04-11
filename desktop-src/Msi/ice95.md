---
description: ICE95 controlla la tabella di controllo e la tabella BBControl per verificare che i controlli Billboard rientrino in tutti i tabelloni.
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14144c7739dfcc1f1b5e66d92d8e6c1c46ed49fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233153"
---
# <a name="ice95"></a>ICE95

ICE95 controlla la [tabella di controllo](control-table.md) e la [tabella BBControl](bbcontrol-table.md) per verificare che i controlli Billboard rientrino in tutti i tabelloni.

## <a name="result"></a>Risultato

Se si verifica una delle condizioni seguenti, un controllo Billboard non è in grado di adattarsi a un tabellone. ICE95 invia gli avvisi seguenti.



| Avviso di ICE95                                                                                                                                                                                                              | Descrizione                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| Elemento BBControl ' \[ 1 \] . \[ 2 \] ' nella tabella BBControl non rientra in tutti i controlli Billboard della tabella dei controlli. La coordinata X supera il limite della larghezza minima del controllo Billboard% s                   | La coordinata X del controllo non rientra nella larghezza del tabellone.                          |
| Elemento BBControl ' \[ 1 \] . \[ 2 \] ' nella tabella BBControl non rientra in tutti i controlli Billboard della tabella dei controlli. La coordinata Y supera il limite dell'altezza minima del controllo Billboard% s                  | La coordinata Y del controllo è sotto la parte inferiore del tabellone.                           |
| Elemento BBControl ' \[ 1 \] . \[ 2 \] ' nella tabella BBControl non rientra in tutti i controlli Billboard della tabella dei controlli. La coordinata X e la larghezza combinate superano la larghezza minima del controllo Billboard% s   | La coordinata X del controllo e la larghezza del controllo non rientrano nella larghezza del tabellone. |
| Elemento BBControl ' \[ 1 \] . \[ 2 \] ' nella tabella BBControl non rientra in tutti i controlli Billboard della tabella dei controlli. La coordinata Y e l'altezza combinate insieme superano l'altezza minima del controllo Billboard% s | La coordinata Y del controllo più l'altezza del controllo si trova sotto la parte inferiore del tabellone. |



 

## <a name="example"></a>Esempio

ICE95 segnala gli avvisi seguenti per l'esempio:

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

Tabella di controllo (parziale) (parziale)



| Control  | Tipo      | Larghezza | Altezza |
|----------|-----------|-------|--------|
| Control1 | Billboard | 300   | 100    |
| Controllo2 | Billboard | 100   | 300    |



 

[Tabella BBControl](bbcontrol-table.md)



| Billboard\_ | BBControl  | X   | S   | Larghezza | Altezza |
|-------------|------------|-----|-----|-------|--------|
| billboard1  | bbcontrol1 | 200 | 0   | 100   | 100    |
| billboard1  | bbcontrol2 | 0   | 200 | 100   | 100    |
| billboard1  | bbcontrol3 | 50  | 0   | 100   | 50     |
| billboard1  | bbcontrol4 | 0   | 50  | 50    | 100    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



