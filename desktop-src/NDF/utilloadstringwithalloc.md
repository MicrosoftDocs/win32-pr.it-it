---
title: Funzione UtilLoadStringWithAlloc (Ndattributils. h)
description: Alloca e carica una stringa fuori dalla tabella delle risorse.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- UtilLoadStringWithAlloc funzione NDF
topic_type:
- apiref
api_name:
- UtilLoadStringWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e13930fe9bb11ae9c9456152c823491eabc462
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121651"
---
# <a name="utilloadstringwithalloc-function"></a>UtilLoadStringWithAlloc (funzione)

La funzione **UtilLoadStringWithAlloc** alloca e carica una stringa fuori dalla tabella delle risorse.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UtilLoadStringWithAlloc(
  _In_  UINT   uID,
  _Out_ LPWSTR *ppwzBuffer,
  _In_  UINT   cchBufferMax
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uID* \[ in\]
</dt> <dd>

Tipo: **uint**

Identificatore della stringa da caricare.

</dd> <dt>

*ppwzBuffer* \[ out\]
</dt> <dd>

Tipo: **LPWSTR \** _

Posizione in cui verrà posizionata la stringa appena allocata. La stringa deve essere liberata usando [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) quando non è più necessaria.

</dd> <dt>

*cchBufferMax* \[ in\]
</dt> <dd>

Tipo: **uint**

Numero massimo di caratteri da caricare dalla tabella delle risorse. Se la stringa di risorsa supera il numero di caratteri specificato, viene troncata e terminata con null.

> [!Note]  
> Questo parametro non può essere impostato su zero.

 

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

[**UtilStringCopyWithAlloc**](utilstringcopywithalloc.md)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

