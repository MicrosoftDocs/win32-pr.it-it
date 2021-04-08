---
description: La proprietà EnableResetOnStop imposta o recupera un valore che determina il modo in cui riprenderà la riproduzione quando il grafico del filtro esegue una transizione da uno stato interrotto.
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: Proprietà EnableResetOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9449d8dd3e2e5ab0e1f008cba3e4cb2aabaa78c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746647"
---
# <a name="enableresetonstop-property"></a>Proprietà EnableResetOnStop

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `EnableResetOnStop` proprietà imposta o recupera un valore che determina il modo in cui riprenderà la riproduzione quando il grafico del filtro esegue una transizione da uno stato interrotto.

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica la posizione in cui l'oggetto MSWebDVD verrà riprodotto dopo l'arresto del grafico del filtro.

## <a name="remarks"></a>Commenti

Si tratta di una proprietà di lettura/scrittura.

I valori possibili di questa proprietà sono: e il valore predefinito è true.



| Valore | Descrizione                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | Il navigatore DVD si reimposta e avvia la riproduzione dall'inizio del disco. Questo è il valore predefinito |
| false | Il navigatore DVD riprenderà la riproduzione da dove era stato interrotto.                                                 |



 

 

 



