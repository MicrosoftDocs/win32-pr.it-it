---
description: La funzione RemoveFromBlob elimina qualsiasi livello di voce BLOB (Proprietario, Categoria o Tag).
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: Funzione RemoveFromBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RemoveFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 09c9c7f5ada320f33d38cd9e935add7e47721c554fbeed11c35a1b73248d963c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063691"
---
# <a name="removefromblob-function"></a>Funzione RemoveFromBlob

La **funzione RemoveFromBlob** elimina qualsiasi livello di voce BLOB (**Owner**, **Category** o **Tag**).

## <a name="syntax"></a>Sintassi


```C++
DWORD RemoveFromBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ Pollici\]
</dt> <dd>

Handle per il BLOB da cui viene eliminata una voce.

</dd> <dt>

*pOwnerName* \[ Pollici\]
</dt> <dd>

Puntatore al **nome del** proprietario.

</dd> <dt>

*pCategoryName* \[ Pollici\]
</dt> <dd>

Puntatore al **nome della** categoria. Un valore di parametro **NULL** indica che il chiamante sta tentando di eliminare le informazioni **sul proprietario** e tutte le relative voci figlio. Si noti che se il valore del parametro *pCategoryName* è **NULL,** anche il *parametro pTagName* deve essere **NULL.**

</dd> <dt>

*pTagName* \[ Pollici\]
</dt> <dd>

Puntatore al **nome del** tag. Un **valore**_null pTagName_ indica che il chiamante sta tentando di eliminare la categoria **specificata** e tutte le relative voci figlio. Se il valore del parametro non **è NULL,** il chiamante chiede solo che le voci **Tag** specificate siano eliminate.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




