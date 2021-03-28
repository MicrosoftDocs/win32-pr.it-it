---
description: Usato per determinare se un elemento è presente in un elenco degli ultimi elementi usati (MRU).
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
ms.openlocfilehash: f95856f6508ad728a15b3df3d6f5eafa4f5bd2ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966876"
---
# <a name="mrucmpproc-callback-function"></a>Funzione di callback MRUCMPPROC

Usato per determinare se un elemento è presente in un elenco degli ultimi elementi usati (MRU).

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

Restituisce 0 se gli elementi sono identici, altrimenti un valore diverso da zero.

## <a name="remarks"></a>Commenti

Questa funzione può essere specificata facoltativamente per l'uso nella struttura [**MRUINFO**](mruinfo.md) passata a [**CreateMRUListW**](createmrulist.md). Questa operazione è utile quando l'elenco MRU è stato creato con il flag **\_ binario MRU** . Quando questa funzione non viene specificata, vengono utilizzate le funzioni di confronto di stringhe standard.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>            |
| Nomi Unicode e ANSI<br/>   | **MRUCMPPROCW** (Unicode) e **MRUCMPPROCA** (ANSI)<br/> |



 

 




