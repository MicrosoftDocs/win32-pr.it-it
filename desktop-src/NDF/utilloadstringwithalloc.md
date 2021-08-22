---
title: Funzione UtilLoadStringWithAlloc (Ndattributils.h)
description: Alloca e carica una stringa dalla tabella delle risorse.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- Funzione UtilLoadStringWithAlloc NDF
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
ms.openlocfilehash: ca649599e2a8a29ecdab2dbbfe2c188947b40487ceb82ab4937622ce82c701a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685611"
---
# <a name="utilloadstringwithalloc-function"></a>Funzione UtilLoadStringWithAlloc

La **funzione UtilLoadStringWithAlloc** alloca e carica una stringa dalla tabella delle risorse.

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

*uID* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Identificatore della stringa da caricare.

</dd> <dt>

*ppwzBuffer* \[ Cambio\]
</dt> <dd>

Tipo: **LPWSTR \***

Posizione in cui verrà inserita la stringa appena allocata. La stringa deve essere liberata [**usando CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) quando non è più necessaria.

</dd> <dt>

*cchBufferMax* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Numero massimo di caratteri da caricare dalla tabella delle risorse. Se la stringa di risorsa è più lunga del numero di caratteri specificato, viene troncata e con terminazione Null.

> [!Note]  
> Questo parametro non può essere impostato su zero.

 

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

[**UtilStringCopyWithAlloc**](utilstringcopywithalloc.md)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

