---
description: La proprietà DVDUniqueID recupera un numero generato dal sistema che identifica in modo univoco il disco corrente.
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: Proprietà DVDUniqueID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488a3e76c93005a55f58e631f0b166b51f036e63857df3b2e21eed6e093e55b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652904"
---
# <a name="dvduniqueid-property"></a>Proprietà DVDUniqueID

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DVDUniqueID` proprietà recupera un numero generato dal sistema che identifica in modo univoco il disco corrente.

``` syntax
[ iDiscID = ] MSWebDVD.DVDUniqueID
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che identifica in modo univoco il disco corrente.

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura senza alcun valore predefinito. Il numero di identificatore (ID) non è assolutamente univoco, ma è univoco per tutti gli scopi pratici. L'ID si applica a tutte le copie replicate di un disco. In altre parole, tutte le copie di un film specifico hanno lo stesso ID. L'ID è basato su dimensioni di file, date e altre informazioni e non sul valore BCA.

 

 



