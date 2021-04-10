---
description: La funzione MergeBlob copia tutte le voci dal BLOB di origine in un BLOB di destinazione.
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: Funzione MergeBlob (Netmon. h)
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
ms.openlocfilehash: 6ea28f5bb6f337b20858baa544c890d5f71bf0c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966772"
---
# <a name="mergeblob-function"></a>MergeBlob (funzione)

La funzione **MergeBlob** copia tutte le voci dal BLOB di origine in un BLOB di destinazione.

## <a name="syntax"></a>Sintassi


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDstBlob* \[ in uscita\]
</dt> <dd>

Handle per il BLOB di destinazione. In input, questo BLOB contiene le informazioni originali. Nell'output questo BLOB contiene le informazioni originali e tutte le informazioni del BLOB di origine.

</dd> <dt>

*hSrcBlob* \[ in\]
</dt> <dd>

Handle per il BLOB di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.

## <a name="remarks"></a>Commenti

Le voci comuni ai file di origine e di destinazione verranno sovrascritte con i dati del BLOB di origine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




