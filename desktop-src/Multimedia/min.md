---
title: Macro min (Minwindef.h)
description: La macro min confronta due valori e restituisce quello più piccolo. Il tipo di dati può essere qualsiasi tipo di dati numerico, signed o unsigned. Il tipo di dati degli argomenti e il valore restituito sono uguali.
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- Macro min Windows Multimedia
topic_type:
- apiref
api_name:
- min
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832adc4a4d326ca8e0689d1ca44ade2e0b77db770cabe6042e42c47e23a44f60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117985673"
---
# <a name="min-macro"></a>min (macro)

La macro **min** confronta due valori e restituisce quello più piccolo. Il tipo di dati può essere qualsiasi tipo di dati numerico, signed o unsigned. Il tipo di dati degli argomenti e il valore restituito sono uguali.

## <a name="syntax"></a>Sintassi


```C++
 min(
    value1,
    value2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value1* 
</dt> <dd>

Specifica il primo di due valori.

</dd> <dt>

*value2* 
</dt> <dd>

Specifica il secondo di due valori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il più piccolo dei due valori specificati.

## <a name="remarks"></a>Commenti

La macro **min** è definita come segue:


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Minwindef.h</dt> </dl> |



 

 





