---
title: macro min (Minwindef. h)
description: La macro min Confronta due valori e restituisce quello più piccolo. Il tipo di dati può essere qualsiasi tipo di dati numerico, con segno o senza segno. Il tipo di dati degli argomenti e il valore restituito sono gli stessi.
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- min macro Windows Multimedia
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
ms.openlocfilehash: b50680d5902ae2dc895f53f023c4b229b03c7e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743927"
---
# <a name="min-macro"></a>min (macro)

La macro **min** Confronta due valori e restituisce quello più piccolo. Il tipo di dati può essere qualsiasi tipo di dati numerico, con segno o senza segno. Il tipo di dati degli argomenti e il valore restituito sono gli stessi.

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

*Value2* 
</dt> <dd>

Specifica il secondo di due valori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il più piccolo dei due valori specificati.

## <a name="remarks"></a>Commenti

La macro **min** viene definita nel modo seguente:


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Minwindef. h</dt> </dl> |



 

 





