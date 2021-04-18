---
description: Crea un delta tra l'origine e la destinazione (forniti come buffer) e restituisce il Delta di output come buffer allocato da MSDelta.
title: CreateDeltaB (funzione)
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: CreateDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: a2142f26499514c24967e5334d782c2dee559cd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324693"
---
# <a name="createdeltab-function"></a>CreateDeltaB (funzione)

Crea un delta tra l'origine e la destinazione (forniti come buffer) e restituisce il Delta di output come buffer allocato da MSDelta.

> [!NOTE]
> È necessario chiamare [DeltaFree](msdelta-deltafree.md) per liberare il buffer di output dopo che questa funzione è stata completata.

## <a name="syntax"></a>Sintassi

```cpp
BOOL  WINAPI  CreateDeltaB(
           DELTA_FILE_TYPE  FileTypeSet,
           DELTA_FLAG_TYPE  SetFlags,
           DELTA_FLAG_TYPE  ResetFlags,
           DELTA_INPUT      Source,
           DELTA_INPUT      Target,
           DELTA_INPUT      SourceOptions,
           DELTA_INPUT      TargetOptions,
           DELTA_INPUT      GlobalOptions,
    const  FILETIME        *lpTargetFileTime,
           ALG_ID           HashAlgId,
           LPDELTA_OUTPUT   lpDelta
    );
```

## <a name="parameters"></a>Parametri

*Filetype*

in Valore [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) che indica il tipo di file impostato da utilizzare per il processo di creazione.

*SetFlags*

in Uno o più valori [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) che specificano i flag da utilizzare durante il processo di creazione, oltre ai flag predefiniti.

*ResetFlags*

in Uno o più valori [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) che specificano i flag predefiniti da reimpostare durante il processo di creazione.

*Origine*

in Struttura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenente un puntatore al buffer che contiene i dati di origine.

*Destinazione*

in Struttura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenente un puntatore al buffer che contiene i dati di destinazione.

*SourceOptions*

[in] Riservato. Passare una struttura di [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con l'oggetto *modificabile* impostato su **false**, *lpStart* impostato su **null** e *uSize* impostato su 0.

*TargetOptions*

[in] Riservato. Passare una struttura di [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con l'oggetto *modificabile* impostato su **false**, *lpStart* impostato su **null** e *uSize* impostato su 0.

*GlobalOptions*

[in] Riservato. Passare una struttura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con *LpStart* impostato su **null** e *uSize* impostato su 0.

*lpTargetFileTime*

in Timestamp impostato sul file di destinazione dopo l'applicazione del Delta. Se **null**, il timestamp di destinazione sarà l'ora corrente durante il processo di creazione.

*HashAlgId*

in ALG_ID dell'algoritmo da utilizzare per generare la firma di destinazione. Alcuni valori speciali sono:

- 0 = nessuna firma
- 32 = CRC a 32 bit definito in msdelta.dll

*lpDelta*

out Puntatore alla struttura [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) in cui deve essere scritto il Delta.

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
