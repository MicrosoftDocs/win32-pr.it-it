---
description: La proprietà EnableResetOnStop imposta o recupera un valore che determina la modalità di ripresa della riproduzione quando il grafico dei filtri esegue una transizione da uno stato arrestato.
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: Proprietà EnableResetOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67be4bfda62839f55dcb4c4597fdad6654072f4dfeb2450c3bce3ed99c13a418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107861"
---
# <a name="enableresetonstop-property"></a>Proprietà EnableResetOnStop

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La proprietà imposta o recupera un valore che determina la modalità di ripresa della riproduzione quando il grafico dei filtri `EnableResetOnStop` esegue una transizione da uno stato arrestato.

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica dove l'oggetto MSWebDVD inizierà di nuovo a riprodurre dopo l'arresto del grafico dei filtri.

## <a name="remarks"></a>Commenti

Si tratta di una proprietà di lettura/scrittura.

I valori possibili di questa proprietà sono: con valore predefinito true.



| Valore | Descrizione                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | DVD Navigator reimposta e avvia la riproduzione dall'inizio del disco. Si tratta del valore predefinito |
| false | Lo strumento di spostamento DVD riprenderà la riproduzione dal punto in cui è stato lasciato.                                                 |



 

 

 



