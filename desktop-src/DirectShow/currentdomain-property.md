---
description: La proprietà CurrentDomain Recupera il dominio DVD in cui si trova l'oggetto MSWebDVD.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: Proprietà CurrentDomain
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead6d61cd622fceac2a4d133a0297892992e763a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481861"
---
# <a name="currentdomain-property"></a>Proprietà CurrentDomain

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `CurrentDomain` proprietà recupera il dominio DVD in cui si trova l'oggetto mswebdvd.

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il dominio corrente.

## <a name="remarks"></a>Commenti

I valori possibili della proprietà sono i seguenti:



| Valore | Descrizione          |
|-------|----------------------|
| 1     | Prima riproduzione           |
| 2     | Menu di gestione video   |
| 3     | Menu set del titolo del video |
| 4     | Titolo                |
| 5     | Interrompere                 |



 

Chiamare questo metodo per assicurarsi che il navigatore DVD si trovi in un dominio valido per il metodo che si sta per chiamare. Ad esempio, prima di chiamare [**PlayTitle**](playtitle-method.md), controllare la `CurrentDomain` proprietà per verificare che il navigatore DVD non sia presente nel dominio stop o First Play.

 

 



