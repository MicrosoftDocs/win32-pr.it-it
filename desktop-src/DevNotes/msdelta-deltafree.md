---
description: Libera il blocco di memoria specificato.
title: DeltaFree (funzione)
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: DeltaFree
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- DeltaFree
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 15885cfa3e879ed6a1e85b2f9553af92d436ca71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328692"
---
# <a name="deltafree-function"></a>DeltaFree (funzione)

Libera il blocco di memoria specificato. È necessario chiamare questa funzione dopo le chiamate a [CreateDeltaB](msdelta-createdeltab.md) e [ApplyDeltaB](msdelta-applydeltab.md) riuscite per liberare il buffer di memoria allocato da msdelta.

## <a name="syntax"></a>Sintassi

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a>Parametri

*lpMemory*

in Blocco di memoria da liberare.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**. Quando la funzione restituisce **false**, è possibile chiamare [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere il codice di errore del sistema Win32 corrispondente.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| Intestazione | msdelta. h |
| DLL | msdelta.dll |
| Unicode | Non applicabile |

## <a name="see-also"></a>Vedi anche

[MSDelta](msdelta.md)

[CreateDeltaB](msdelta-createdeltab.md)

[ApplyDeltaB](msdelta-applydeltab.md)
