---
title: Tipo semplice LengthType
description: Definisce un tipo di lunghezza utilizzato per specificare il numero di byte o caratteri in un elemento di dati a lunghezza variabile, ad esempio dati binari o una stringa ANSI o Unicode.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- Tipo semplice LengthType EventLog
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9ded861e3e46cd5e4fc6c069d95bba9f0ab3457559bf319aef41cdf906e193b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997861"
---
# <a name="lengthtype-simple-type"></a>Tipo semplice LengthType

Definisce un tipo di lunghezza utilizzato per specificare il numero di byte o caratteri in un elemento di dati a lunghezza variabile, ad esempio dati binari o una stringa ANSI o Unicode. Il valore può essere specificato come valore xs:unsignedShort o come stringa che fa riferimento al nome del nodo dell'elemento di dati che contiene il valore short senza segno.

``` syntax
<xs:simpleType name="LengthType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





