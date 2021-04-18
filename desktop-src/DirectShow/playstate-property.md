---
description: La proprietà riproduzione recupera lo stato corrente dell'oggetto MSWebDVD.
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: Proprietà riproduzione
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8c699ce3f232f9afc14472f0308fa65adc6abb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303985"
---
# <a name="playstate-property"></a>Proprietà riproduzione

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `PlayState` proprietà recupera lo stato corrente dell'oggetto **mswebdvd** .

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta lo stato corrente del navigatore DVD.



| Codice restituito | Descrizione   |
|-------------|---------------|
| -2          | Non definito     |
| -1          | Inizializzazione annullata |
| 0           | Arrestato       |
| 1           | Paused        |
| 2           | In esecuzione       |



 

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura e non prevede alcun valore predefinito.

L'oggetto **mswebdvd** controlla il filtro del navigatore DirectShow DVD, che esegue il lavoro effettivo della navigazione in DVD. Si tratta in realtà dello stato del navigatore DVD a cui questa proprietà fa riferimento. Il navigatore DVD può trovarsi in uno dei diversi Stati, come descritto in precedenza. La `PlayState` proprietà può essere utile come strumento di diagnostica, ma in genere non dovrebbe essere necessario che un'applicazione di scripting monitori lo stato del navigatore DVD.

 

 



