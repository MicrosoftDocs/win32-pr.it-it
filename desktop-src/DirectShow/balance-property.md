---
description: La proprietà Balance imposta o Recupera il saldo del altoparlante per l'output del flusso audio.
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: Proprietà Balance
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1334fcc51695f04ab0026ded8c68c17cb07aa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304262"
---
# <a name="balance-property"></a>Proprietà Balance

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `Balance` proprietà imposta o Recupera il saldo del altoparlante per l'output del flusso audio.

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta i livelli di bilanciamento. L'intervallo di input consentito è compreso tra-10.000 e 10.000. Un valore pari a 0 imposta un saldo neutro, ovvero gli altoparlanti sinistro e destro ricevono lo stesso segnale audio di ampiezza.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura e il valore predefinito è 0, vale a dire che entrambi gli speaker ricevono segnali audio equivalenti. Come per la proprietà [**volume**](volume-property.md) , le unità corrispondono a .01 decibel (moltiplicato per-1 quando


```
iBalance
```



è un valore positivo). Ad esempio, il valore 1000 indica 10 dB sul canale destro e 90 dB sul canale sinistro.

 

 



