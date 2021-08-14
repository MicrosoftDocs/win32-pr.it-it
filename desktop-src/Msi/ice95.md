---
description: ICE95 controlla la tabella di controllo e la tabella BBControl per verificare che i controlli dei manifesti si adattino a tutti i manifesti.
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f0f7d44554385c33648036f314406971193afc079b5aa8e72cf595695797ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315261"
---
# <a name="ice95"></a>ICE95

ICE95 controlla la [tabella di controllo](control-table.md) e la tabella [BBControl](bbcontrol-table.md) per verificare che i controlli dei manifesti si adattino a tutti i manifesti.

## <a name="result"></a>Risultato

Se una delle condizioni seguenti è vera, un controllo di tipo manifesto non può essere inserirsi in un manifesto pubblicitario. ICE95 invia gli avvisi seguenti.



| Avviso ICE95                                                                                                                                                                                                              | Descrizione                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| L'elemento BBControl ' \[ 1 \] . \[ 2 \] ' nella tabella BBControl non rientra in tutti i controlli della tabella Control. La coordinata X supera il limite della larghezza minima del controllo barra verticale %s                   | La coordinata X del controllo non rientra nella larghezza del manifesto.                          |
| L'elemento BBControl ' \[ 1 \] . \[ 2 \] ' nella tabella BBControl non rientra in tutti i controlli della tabella Control. La coordinata Y supera il limite dell'altezza minima del controllo barra verticale %s                  | La coordinata Y del controllo si trova sotto la parte inferiore del manifesto.                           |
| L'elemento BBControl ' \[ 1 \] . \[ 2 \] ' nella tabella BBControl non rientra in tutti i controlli della tabella Control. La coordinata X e la larghezza combinate superano la larghezza minima del controllo barra verticale %s   | La coordinata X del controllo e la larghezza del controllo si trova all'esterno della larghezza del pannello. |
| L'elemento BBControl ' \[ 1 \] . \[ 2 \] ' nella tabella BBControl non rientra in tutti i controlli della tabella Control. La coordinata Y e l'altezza combinate superano l'altezza minima del controllo %s | La coordinata Y del controllo e l'altezza del controllo si trova sotto la parte inferiore del manifesto. |



 

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
| control1 | Billboard | 300   | 100    |
| Controllo2 | Billboard | 100   | 300    |



 

[Tabella BBControl](bbcontrol-table.md)



| Billboard\_ | BBControl  | X   | S   | Larghezza | Altezza |
|-------------|------------|-----|-----|-------|--------|
| manifesto1  | bbcontrol1 | 200 | 0   | 100   | 100    |
| manifesto1  | bbcontrol2 | 0   | 200 | 100   | 100    |
| manifesto1  | bbcontrol3 | 50  | 0   | 100   | 50     |
| manifesto1  | bbcontrol4 | 0   | 50  | 50    | 100    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



