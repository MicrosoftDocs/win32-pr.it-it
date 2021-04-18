---
title: Tipo semplice LengthType
description: Definisce un tipo di lunghezza utilizzato per specificare il numero di byte o caratteri di un elemento di dati a lunghezza variabile, ad esempio dati binari o una stringa ANSI o Unicode.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- Log eventi di tipo semplice LengthType
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dbb0720c2e26fa73056ccffdd17392e93e491c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341203"
---
# <a name="lengthtype-simple-type"></a>Tipo semplice LengthType

Definisce un tipo di lunghezza utilizzato per specificare il numero di byte o caratteri di un elemento di dati a lunghezza variabile, ad esempio dati binari o una stringa ANSI o Unicode. Il valore può essere specificato come valore xs: unsignedShort o come stringa che fa riferimento al nome del nodo dell'elemento dati che contiene il valore short senza segno.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





