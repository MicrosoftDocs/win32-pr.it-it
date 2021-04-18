---
title: macro max (Minwindef. h)
description: La macro max Confronta due valori e restituisce quello più grande. Il tipo di dati può essere qualsiasi tipo di dati numerico, con segno o senza segno. Il tipo di dati degli argomenti e il valore restituito sono gli stessi.
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- Max macro Windows Multimedia
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
ms.openlocfilehash: b484f2505958aca04745c63ca63a0dd131a51ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517632"
---
# <a name="max-macro"></a>max (macro)

La macro **Max** Confronta due valori e restituisce quello più grande. Il tipo di dati può essere qualsiasi tipo di dati numerico, con segno o senza segno. Il tipo di dati degli argomenti e il valore restituito sono gli stessi.

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

*Value2* 
</dt> <dd>

Specifica il secondo di due valori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il maggiore dei due valori specificati.

## <a name="remarks"></a>Commenti

La macro **Max** è definita come segue:


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Minwindef. h</dt> </dl> |



 

 





