---
description: L'evento ReadyStateChange viene inviato quando la proprietà ReadyState del controllo MSWebDVD viene modificata.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: ReadyStateChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f73e0b5b7cd7178df31b3f6efda56e398d8cb406598355a3c49702714686af3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697121"
---
# <a name="readystatechange"></a>ReadyStateChange

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

`ReadyStateChange`L'evento viene inviato quando la proprietà **ReadyState** del controllo MSWebDVD viene modificata.

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*
</dt> <dd>

Specifica il nuovo valore della [**proprietà ReadyState.**](readystate-property.md)



| Valore | Descrizione               |
|-------|---------------------------|
| 0     | READYSTATE \_ UNINITIALIZED |
| 1     | CARICAMENTO \_ READYSTATE       |
| 2     | READYSTATE \_ CARICATO        |
| 3     | READYSTATE \_ INTERACTIVE   |
| 4     | READYSTATE \_ COMPLETE      |



 

</dd> </dl>

 

 



