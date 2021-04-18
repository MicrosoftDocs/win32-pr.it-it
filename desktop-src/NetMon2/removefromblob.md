---
description: La funzione RemoveFromBlob elimina qualsiasi livello di voce del BLOB (proprietario, categoria o tag).
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: Funzione RemoveFromBlob (Netmon. h)
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
ms.openlocfilehash: a23e4e7e6e6d5c85b1284f8aaba49c1f8eae728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306555"
---
# <a name="removefromblob-function"></a>RemoveFromBlob (funzione)

La funzione **RemoveFromBlob** elimina qualsiasi livello di voce del BLOB (**proprietario**, **categoria** o **tag**).

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

*hBlob* \[ in\]
</dt> <dd>

Handle per il BLOB da cui viene eliminata una voce.

</dd> <dt>

*pOwnerName* \[ in\]
</dt> <dd>

Puntatore al nome del **proprietario** .

</dd> <dt>

*pCategoryName* \[ in\]
</dt> <dd>

Puntatore al nome della **categoria** . Un valore di parametro **null** indica che il chiamante sta provando a eliminare le informazioni sul **proprietario** specificate e tutte le relative voci figlio. Si noti che se il valore del parametro *pCategoryName* è **null**, anche il parametro *pTagName* deve essere **null**.

</dd> <dt>

*pTagName* \[ in\]
</dt> <dd>

Puntatore al nome del **tag** . Un valore _PTagName_ **null** indica che il chiamante sta provando a eliminare la **categoria** specificata e tutte le relative voci figlio. Se il valore del parametro non è **null**, il chiamante chiede che vengano eliminate solo le voci di **tag** specificate.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




