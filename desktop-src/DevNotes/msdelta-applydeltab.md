---
description: Usa il Delta e l'origine (forniti come buffer) per creare una nuova copia dei dati di destinazione. I dati di output vengono restituiti in un buffer allocato da MSDelta.
title: ApplyDeltaB (funzione)
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: ApplyDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplyDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 368788ba894064aa8ac3f8c9711f987a32f306af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331466"
---
# <a name="applydeltab-function"></a>ApplyDeltaB (funzione)

Usa il Delta e l'origine (forniti come buffer) per creare una nuova copia dei dati di destinazione. I dati di output vengono restituiti in un buffer allocato da MSDelta.

> [!NOTE]
> È necessario chiamare [DeltaFree](msdelta-deltafree.md) per liberare il buffer di output dopo che questa funzione è stata completata.

> [!NOTE]
> Se il delta specificato è stato creato con [PatchAPI](patchapi.md)e viene impostato il FLAG di [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) , msdelta chiamerà PatchAPI per applicare il Delta.

## <a name="syntax"></a>Sintassi

```cpp
BOOL  WINAPI  ApplyDeltaB(
    DELTA_FLAG_TYPE  ApplyFlags,
    DELTA_INPUT      Source,
    DELTA_INPUT      Delta,
    LPDELTA_OUTPUT   lpTarget
   );
```

## <a name="parameters"></a>Parametri

*ApplyFlags*

in [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) o [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).

*Origine*

in Struttura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenente un puntatore al buffer che contiene i dati di origine.

*Delta*

in Struttura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenente un puntatore al buffer che contiene i dati Delta.

*lpTarget*

out Puntatore alla struttura [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) in cui deve essere scritta la destinazione.

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

[DeltaFree](msdelta-deltafree.md)
