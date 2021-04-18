---
description: Crea un delta tra il file di origine specificato e il file di destinazione specificato.
title: Funzione CreatePatchFileExA/W
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: CreatePatchFileExA, CreatePatchFileExW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePatchFileExW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: c84be2d859a780e46e7e940aa4a7e7da5296f0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324441"
---
# <a name="createpatchfileexaw-function"></a>Funzione CreatePatchFileExA/W

Le funzioni **CreatePatchFileExA** e **CreatePatchFileExW** creano un delta tra il file di origine specificato e il file di destinazione specificato. I file di origine e di destinazione vengono forniti come percorsi. Anche il Delta di output viene scritto in un percorso specificato. Queste funzioni forniscono report sullo stato di avanzamento durante il processo di creazione.

## <a name="syntax"></a>Sintassi

```cpp
BOOL  PATCHAPI  CreatePatchFileExA(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCTSTR                   NewFileName,
    LPCTSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );

BOOL  PATCHAPI  CreatePatchFileExW(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCWSTR                   NewFileName,
    LPCWSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );
```

## <a name="parameters"></a>Parametri

*OldFileCount*

Numero totale di file di origine. Utilizzato per creare Delta rispetto a più file di origine (massimo 255).

*OldFileInfoArray*

Puntatore alla matrice di informazioni sul file di origine.

*Nomenuovofile*

Nome del file di destinazione.

*PatchFileName*

Nome del Delta creato.

*OptionFlags*

Flag di creazione.

*ProgressCallback*

Puntatore al callback di stato definito dall'applicazione.

*CallbackContext*

Puntatore al contesto definito dall'applicazione.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| Intestazione | PatchAPI. h |
| DLL | mspatchc.dll |
| Unicode | Implementato come CreatePatchFileExW (Unicode) e CreatePatchFileExA (ANSI) |

## <a name="see-also"></a>Vedi anche

[PatchAPI](patchapi.md)
