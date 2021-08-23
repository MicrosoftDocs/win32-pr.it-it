---
description: La proprietà CurrentDomain recupera il dominio DVD in cui si trova l'oggetto MSWebDVD.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: Proprietà CurrentDomain
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf022d44cc3580a4d5208c5bc96413dfa445b0f2fcbf74eeb938ee77fa0677bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953390"
---
# <a name="currentdomain-property"></a>Proprietà CurrentDomain

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `CurrentDomain` proprietà recupera il dominio DVD in cui si trova l'oggetto MSWebDVD.

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il dominio corrente.

## <a name="remarks"></a>Commenti

I valori possibili della proprietà sono:



| Valore | Descrizione          |
|-------|----------------------|
| 1     | Prima riproduzione           |
| 2     | Menu Gestione video   |
| 3     | Menu Del set di titoli video |
| 4     | Titolo                |
| 5     | Interrompere                 |



 

Chiamare questo metodo per assicurarsi che dvd Navigator si trova in un dominio valido per il metodo che si sta per chiamare. Ad esempio, prima di chiamare [**PlayTitle**](playtitle-method.md), controllare la proprietà per assicurarsi che lo strumento di navigazione DVD non sia `CurrentDomain` nel dominio Stop o First Play.

 

 



