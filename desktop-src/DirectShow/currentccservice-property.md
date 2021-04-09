---
description: La proprietà CurrentCCService imposta o Recupera il servizio di Captioning chiuso corrente.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: Proprietà CurrentCCService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5c1ddf243b0ec943be1f22930a8802d28d1bda
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876705"
---
# <a name="currentccservice-property"></a>Proprietà CurrentCCService

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `CurrentCCService` proprietà imposta o Recupera il servizio di didascalia corrente chiuso.

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore integer che indica il tipo di servizio di didascalia chiuso abilitato.

## <a name="remarks"></a>Commenti

I valori possibili di questa proprietà sono:



| Valore | Descrizione                                                          |
|-------|----------------------------------------------------------------------|
| 0x0   | Nessun servizio corrente. Si tratta del valore predefinito.                       |
| 0x1   | Didascalia vera, primo campo. Servizio predefinito.                       |
| 0x2   | Didascalia per lingua secondaria, secondo campo. Generalmente non utilizzato. |



 

Si tratta di una proprietà di lettura/scrittura.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CCActive**](ccactive-property.md)
</dt> </dl>

 

 



