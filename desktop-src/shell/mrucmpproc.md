---
description: Usato per determinare se un elemento è presente in un elenco degli elementi usati più di recente.
title: Funzione di callback MRUCMPPROC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MRUCMPPROC
- MRUCMPPROCA
- MRUCMPPROCW
api_type:
- UserDefined
api_location: ''
ms.assetid: 00f31d6b-2a96-4abd-9647-24a6e66aa22f
ms.openlocfilehash: bcf8bb7c8ec4ceab299efd75c61cabe86f43d0ee46585be59ab4000957554ed2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111491"
---
# <a name="mrucmpproc-callback-function"></a>Funzione di callback MRUCMPPROC

Usato per determinare se un elemento è presente in un elenco degli elementi usati più di recente.

## <a name="syntax"></a>Sintassi


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pString1* 
</dt> <dd>

Tipo: **LPCTSTR**

Prima stringa.

</dd> <dt>

*pString2* 
</dt> <dd>

Tipo: **LPCTSTR**

Seconda stringa da confrontare con la prima.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Restituisce 0 se gli elementi sono identici; in caso contrario, un valore diverso da zero.

## <a name="remarks"></a>Commenti

Questa funzione può essere specificata facoltativamente per l'uso nella [**struttura MRUINFO**](mruinfo.md) passata [**a CreateMRUListW.**](createmrulist.md) Ciò è utile quando l'elenco MRU è stato creato con il flag **MRU \_ BINARY.** Quando questa funzione non viene specificata, vengono usate le funzioni standard di confronto tra stringhe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>            |
| Nomi Unicode e ANSI<br/>   | **MRUCMPPROCW** (Unicode) e **MRUCMPPROCA** (ANSI)<br/> |



 

 




