---
title: Funzione UtilStringCopyWithAlloc (Ndattributils. h)
description: Alloca e copia una stringa di origine.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- UtilStringCopyWithAlloc funzione NDF
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
ms.openlocfilehash: b68bd1815ff09473f0431dde19a12a87603a9dec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301357"
---
# <a name="utilstringcopywithalloc-function"></a>UtilStringCopyWithAlloc (funzione)

La funzione **UtilStringCopyWithAlloc** alloca e copia una stringa di origine.

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

*Buffer* \[ out\]
</dt> <dd>

Tipo: **LPWSTR \** _

Posizione in cui è archiviato il puntatore alla memoria allocata. Quando non è più necessario, è necessario rilasciarlo con [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree). Questo buffer è sempre con terminazione null.

</dd> <dt>

*BufferMax* \[ in\]
</dt> <dd>

Tipo: **uint**

Numero massimo di caratteri da leggere dall' *origine*.

</dd> <dt>

*Origine* \[ dati in\]
</dt> <dd>

Tipo: **LPCWSTR**

Stringa da copiare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

I valori restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice restituito                                                                                  | Descrizione                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Operazione completata.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o più parametri non sono stati specificati correttamente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                 |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> </dl>

 

