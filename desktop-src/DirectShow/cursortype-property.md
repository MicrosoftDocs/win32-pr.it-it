---
description: La proprietà CursorType imposta o Recupera il tipo di cursore corrente.
ms.assetid: f362e790-a7c7-4fb6-86f3-7cd25f78fe0e
title: Proprietà CursorType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c17ae74c471bebe6da2bcef4d22d7c247f4eda1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876585"
---
# <a name="cursortype-property"></a>Proprietà CursorType

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `CursorType` proprietà imposta o Recupera il tipo di cursore corrente.

``` syntax
[ iCursorType = ] MSWebDVD.CursorType
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il tipo di cursore.

## <a name="remarks"></a>Commenti

I valori possibili per questa proprietà sono:



| Valore | Descrizione |
|-------|-------------|
| 0     | Freccia       |
| 1     | Zoom avanti     |
| 2     | Zoom indietro    |
| 3     | A sinistra        |
| -1    | nessuno        |



 

Questa proprietà è di lettura/scrittura e il valore predefinito è zero. Quando l'immagine viene ingrandita, l'impostazione `CursorType` su **Hand** (0x3) consente di attivare la modalità di trascinamento dell'applicazione, consentendo all'utente di spostare l'immagine all'interno dell'area di visualizzazione del video.

 

 



