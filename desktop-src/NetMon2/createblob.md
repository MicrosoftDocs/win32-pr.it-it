---
description: La funzione CreateBlob crea un BLOB vuoto.
ms.assetid: fa31855b-af85-4ab5-b434-e54111731d8f
title: Funzione CreateBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 1c5a74a2008993aba40b97e6fce779398132dbeae0428d4c7ae2054640a4159a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744711"
---
# <a name="createblob-function"></a>Funzione CreateBlob

La **funzione CreateBlob** crea un BLOB vuoto.

## <a name="syntax"></a>Sintassi


```C++
DWORD CreateBlob(
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phBlob* \[ Cambio\]
</dt> <dd>

Puntatore alla variabile in cui viene restituito il puntatore al nuovo BLOB.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che descrive l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DestroyBlob](destroyblob.md)
</dt> </dl>

 

 




