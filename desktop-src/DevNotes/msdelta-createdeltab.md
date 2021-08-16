---
description: Crea un delta tra l'origine e la destinazione (forniti come buffer) e restituisce il delta di output come buffer allocato da MSDelta.
title: Funzione CreateDeltaB
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
ms.openlocfilehash: ae13dfb82d4699bbb8cc222b4cd1aaa2615e8efaa578de60483f00552faf2086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826925"
---
# <a name="createdeltab-function"></a>Funzione CreateDeltaB

Crea un delta tra l'origine e la destinazione (forniti come buffer) e restituisce il delta di output come buffer allocato da MSDelta.

> [!NOTE]
> È necessario chiamare [DeltaFree](msdelta-deltafree.md) per liberare il buffer di output dopo il completamento di questa funzione.

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

*FileTypeSet*

[in] Valore [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) che indica il tipo di file impostato da usare per il processo di creazione.

*SetFlags*

[in] Uno o più [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) che specificano i flag da usare durante il processo di creazione, oltre ai flag predefiniti.

*ResetFlags*

[in] Uno o più valori [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) che specificano i flag predefiniti da reimpostare durante il processo di creazione.

*Origine*

[in] Struttura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenente un puntatore al buffer contenente i dati di origine.

*Destinazione*

[in] Struttura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenente un puntatore al buffer contenente i dati di destinazione.

*SourceOptions*

[in] Riservato. Passare una [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con *Editable* impostato su **FALSE,** *lpStart* impostato su **NULL** e *uSize* impostato su 0.

*TargetOptions*

[in] Riservato. Passare una [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con *Editable* impostato su **FALSE,** *lpStart* impostato su **NULL** e *uSize* impostato su 0.

*GlobalOptions*

[in] Riservato. Passare una [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) struttura con *lpStart* impostato su **NULL** e *uSize* impostato su 0.

*lpTargetFileTime*

[in] Timestamp impostato nel file di destinazione dopo l'applicazione del delta. Se **NULL,** il timestamp di destinazione sarà l'ora corrente durante il processo di creazione.

*HashAlgId*

[in] ALG_ID dell'algoritmo da usare per generare la firma di destinazione. Alcuni valori speciali sono:

- 0 = Nessuna firma
- 32 = CRC a 32 bit definito in msdelta.dll

*lpDelta*

[out] Puntatore alla [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) struttura in cui deve essere scritto il delta.

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
