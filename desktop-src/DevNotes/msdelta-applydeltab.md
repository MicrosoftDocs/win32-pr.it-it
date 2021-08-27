---
description: Usa il delta e l'origine (forniti come buffer) per creare una nuova copia dei dati di destinazione. I dati di output vengono restituiti in un buffer allocato da MSDelta.
title: Funzione ApplyDeltaB
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
ms.openlocfilehash: 2a6034ca101a192be66db1b16a4ac7b27e7288d9453dfaaab5782e55e11d4c67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079761"
---
# <a name="applydeltab-function"></a>Funzione ApplyDeltaB

Usa il delta e l'origine (forniti come buffer) per creare una nuova copia dei dati di destinazione. I dati di output vengono restituiti in un buffer allocato da MSDelta.

> [!NOTE]
> È necessario chiamare [DeltaFree](msdelta-deltafree.md) per liberare il buffer di output dopo il completamento di questa funzione.

> [!NOTE]
> Se il delta specificato è stato creato usando [PatchAPI](patchapi.md)e il flag [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) è impostato, MSDelta chiamerà PatchAPI per applicare il delta.

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

[in] È [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) o [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).

*Origine*

[in] Struttura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenente un puntatore al buffer contenente i dati di origine.

*Delta*

[in] Struttura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenente un puntatore al buffer contenente i dati differenziali.

*lpTarget*

[out] Puntatore alla [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) struttura in cui deve essere scritta la destinazione.

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

[DeltaFree](msdelta-deltafree.md)
