---
description: L'evento ReadyStateChange viene inviato quando viene modificata la proprietà ReadyState del controllo MSWebDVD.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: ReadyStateChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46cc8d7ffdee650aac48839d49ed8162e10bb955
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522049"
---
# <a name="readystatechange"></a>ReadyStateChange

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

L' `ReadyStateChange` evento viene inviato quando la proprietà **ReadyState** del controllo mswebdvd è cambiata.

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*
</dt> <dd>

Specifica il nuovo valore della proprietà [**ReadyState**](readystate-property.md) .



| Valore | Descrizione               |
|-------|---------------------------|
| 0     | READYSTATE non \_ inizializzato |
| 1     | \_caricamento readyState       |
| 2     | READYSTATE \_ caricato        |
| 3     | READYSTATE \_ interattivo   |
| 4     | READYSTATE \_ completata      |



 

</dd> </dl>

 

 



