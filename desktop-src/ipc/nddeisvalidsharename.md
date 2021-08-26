---
description: Determina se un nome di condivisione usa la sintassi corretta.
ms.assetid: 4ffcff5d-0db5-4761-a31a-acefd2b8d9e2
title: Funzione NDdeIsValidShareName (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidShareName
- NDdeIsValidShareNameA
- NDdeIsValidShareNameW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 3e289429047d8d1cee4f525a9f45a9abe1dd8eb51bcf57e83e39876fba9a5a89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964001"
---
# <a name="nddeisvalidsharename-function"></a>Funzione NDdeIsValidShareName

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

Determina se un nome di condivisione usa la sintassi corretta.

## <a name="syntax"></a>Sintassi


```C++
BOOL NDdeIsValidShareName(
  _In_ LPTSTR shareName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*shareName* \[ Pollici\]
</dt> <dd>

Nome della condivisione da convalidare. Questo parametro non può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il nome della condivisione ha una sintassi valida, il valore restituito è diverso da zero.

Se il nome della condivisione non ha una sintassi valida, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Questa funzione viene chiamata anche da [**NDdeShareAdd**](nddeshareadd.md) quando crea la condivisione DDE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeIsValidShareNameW** (Unicode) e **NDdeIsValidShareNameA** (ANSI)<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica Dynamic Data Exchange rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




