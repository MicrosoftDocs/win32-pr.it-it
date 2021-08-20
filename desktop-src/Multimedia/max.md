---
title: Macro max (Minwindef.h)
description: La macro max confronta due valori e restituisce quello più grande. Il tipo di dati può essere qualsiasi tipo di dati numerico, signed o unsigned. Il tipo di dati degli argomenti e il valore restituito sono uguali.
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- max macro Windows Multimedia
topic_type:
- apiref
api_name:
- max
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc592fcc588c14ee04c1f595c5b5bc95c860b2ab0b761906886010db478d5f1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138647"
---
# <a name="max-macro"></a>max (macro)

La macro **max** confronta due valori e restituisce quello più grande. Il tipo di dati può essere qualsiasi tipo di dati numerico, signed o unsigned. Il tipo di dati degli argomenti e il valore restituito sono uguali.

## <a name="syntax"></a>Sintassi


```C++
 max(
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

Il valore restituito è il maggiore dei due valori specificati.

## <a name="remarks"></a>Commenti

La macro **max** viene definita come segue:


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Minwindef.h</dt> </dl> |



 

 





