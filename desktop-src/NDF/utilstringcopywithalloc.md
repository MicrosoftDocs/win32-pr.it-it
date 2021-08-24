---
title: Funzione UtilStringCopyWithAlloc (Ndattributils.h)
description: Alloca e copia una stringa di origine.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- Funzione UtilStringCopyWithAlloc NDF
topic_type:
- apiref
api_name:
- UtilStringCopyWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3654fa5eefd45a51d963325e10fbcba765420afe25a5c47a058bbaf4e4093ef0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801531"
---
# <a name="utilstringcopywithalloc-function"></a>Funzione UtilStringCopyWithAlloc

La **funzione UtilStringCopyWithAlloc** alloca e copia una stringa di origine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UtilStringCopyWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR Source
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Buffer* \[ Cambio\]
</dt> <dd>

Tipo: **LPWSTR \***

Posizione in cui è archiviato il puntatore alla memoria allocata. Quando non è più necessario, deve essere rilasciato con [**CoTaskMemFree.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) Questo buffer ha sempre terminazione Null.

</dd> <dt>

*BufferMax* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Numero massimo di caratteri da leggere da *Source.*

</dd> <dt>

*Origine* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Stringa da copiare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

I valori restituiti possibili includono, ma non sono limitati, i seguenti.



| Codice restituito                                                                                  | Descrizione                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o più parametri non sono stati specificati correttamente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> </dl>

 

