---
description: Libera il blocco di memoria specificato.
title: Funzione DeltaFree
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
ms.openlocfilehash: 606b8d91d20c74f7dd56ff4e09986abec3eef547989990a38bd8b4e3a27382c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079731"
---
# <a name="deltafree-function"></a>Funzione DeltaFree

Libera il blocco di memoria specificato. È necessario chiamare questa funzione dopo le chiamate riuscite [a CreateDeltaB](msdelta-createdeltab.md) e [ApplyDeltaB](msdelta-applydeltab.md) per liberare il buffer di memoria allocato da MSDelta.

## <a name="syntax"></a>Sintassi

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a>Parametri

*lpMemory*

[in] Blocco di memoria da liberare.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **TRUE** se ha esito positivo. In caso contrario, restituisce **FALSE.** Quando la funzione restituisce **FALSE,** è possibile chiamare [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere il codice di errore di sistema Win32 corrispondente.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| Intestazione | msdelta.h |
| DLL | msdelta.dll |
| Unicode | Non applicabile |

## <a name="see-also"></a>Vedi anche

[MSDelta](msdelta.md)

[CreateDeltaB](msdelta-createdeltab.md)

[ApplyDeltaB](msdelta-applydeltab.md)
