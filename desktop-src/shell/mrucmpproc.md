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
ms.openlocfilehash: 83020fbcd0d4cfcfbc643d1360e3671595de6f32
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840782"
---
# <a name="mrucmpproc-callback-function"></a>Funzione di callback MRUCMPPROC

Consente di determinare se un elemento è presente in un elenco degli elementi usati più di recente.

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

Restituisce 0 se gli elementi sono identici. In caso contrario, un valore diverso da zero.

## <a name="remarks"></a>Commenti

Questa funzione può essere facoltativamente specificata per l'uso nella [**struttura MRUINFO**](mruinfo.md) passata [**a CreateMRUListW.**](createmrulist.md) Ciò è utile quando l'elenco MRU è stato creato con il flag **BINARY MRU. \_** Quando questa funzione non viene specificata, vengono usate le funzioni di confronto di stringhe standard.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>            |
| Nomi Unicode e ANSI<br/>   | **MRUCMPPROCW** (Unicode) e **MRUCMPPROCA** (ANSI)<br/> |



 

 




