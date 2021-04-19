---
description: La funzione DestroyBlob libera tutta la memoria associata al BLOB e quindi Elimina il BLOB.
ms.assetid: 46cde0b7-1b59-426e-b19b-3c73af3d461a
title: Funzione DestroyBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e90630981c16f38d601d4e06d04f9326174ef721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317751"
---
# <a name="destroyblob-function"></a>DestroyBlob (funzione)

La funzione **DestroyBlob** libera tutta la memoria associata al BLOB e quindi Elimina il BLOB.

## <a name="syntax"></a>Sintassi


```C++
DWORD DestroyBlob(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ in\]
</dt> <dd>

Handle per il BLOB che viene eliminato definitivamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che descrive l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[CreateBlob](createblob.md)
</dt> </dl>

 

 




