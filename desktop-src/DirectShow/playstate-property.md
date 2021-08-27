---
description: La proprietà PlayState recupera lo stato corrente dell'oggetto MSWebDVD.
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: Proprietà PlayState
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b66ae0ddfb1a8ceb296ec647a0149a42de68f635ffd198d6ba6609ff11e4888
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102351"
---
# <a name="playstate-property"></a>Proprietà PlayState

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `PlayState` proprietà recupera lo stato corrente dell'oggetto **MSWebDVD.**

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore Integer che rappresenta lo stato corrente dello strumento di navigazione DVD.



| Codice restituito | Descrizione   |
|-------------|---------------|
| -2          | Non definito     |
| -1          | Inizializzazione annullata |
| 0           | Arrestato       |
| 1           | Paused        |
| 2           | In esecuzione       |



 

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura senza alcun valore predefinito.

**L'oggetto MSWebDVD** controlla il DirectShow DVD Navigator, che esegue le operazioni effettive di navigazione dei DVD. È in realtà lo stato dello strumento di navigazione DVD a cui fa riferimento questa proprietà. Il DVD Navigator può essere in uno dei diversi stati, come descritto in precedenza. La proprietà può essere utile come strumento di diagnostica, ma in genere non deve essere necessario che un'applicazione di scripting monitori lo stato dello `PlayState` strumento di spostamento DVD.

 

 



