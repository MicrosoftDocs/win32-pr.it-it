---
description: La funzione MergeBlob copia tutte le voci dal BLOB di origine in un BLOB di destinazione.
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: Funzione MergeBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5c0ce93235a0c46286b9bfbef0773a5584f3db774aa52991b4e0eaa9dd38352f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677191"
---
# <a name="mergeblob-function"></a>Funzione MergeBlob

La **funzione MergeBlob** copia tutte le voci dal BLOB di origine in un BLOB di destinazione.

## <a name="syntax"></a>Sintassi


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDstBlob* \[ in, out\]
</dt> <dd>

Handle per il BLOB di destinazione. Nell'input, questo BLOB contiene le informazioni originali. Nell'output, questo BLOB contiene le informazioni originali più tutte le informazioni del BLOB di origine.

</dd> <dt>

*hSrcBlob* \[ Pollici\]
</dt> <dd>

Handle per il BLOB di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.

## <a name="remarks"></a>Commenti

Le voci comuni ai file di origine e di destinazione verranno sovrascritte con i dati del BLOB di origine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




