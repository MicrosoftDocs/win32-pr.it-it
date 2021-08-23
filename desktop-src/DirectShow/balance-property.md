---
description: La proprietà Balance imposta o recupera il bilanciamento del parlante per l'output del flusso audio.
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: Proprietà Balance
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4faa8bcacb8c4603dcb67ee6cc617ced4b31bd7afa3afa16d3ba3831040a004
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689381"
---
# <a name="balance-property"></a>Proprietà Balance

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `Balance` proprietà imposta o recupera il bilanciamento del parlante per l'output del flusso audio.

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta i livelli di bilanciamento. L'intervallo di input consentito è compreso tra -10.000 e 10.000. Il valore 0 imposta un bilanciamento neutro, che sia gli altoparlanti a sinistra che a destra hanno lo stesso segnale audio di ampiezza.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura con un valore predefinito pari a 0, vale a dire che entrambi gli altoparlanti ricevono segnali audio equivalenti. Come per la [**proprietà Volume,**](volume-property.md) le unità corrispondono ai decibel .01 (moltiplicati per -1 quando


```
iBalance
```



è un valore positivo. Ad esempio, il valore 1000 indica 10 dB sul canale destro e 90 dB sul canale sinistro.

 

 



