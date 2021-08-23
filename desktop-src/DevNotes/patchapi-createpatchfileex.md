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
ms.openlocfilehash: 7d73b6f4d10c52e9eca147227fdbfece31cba157af84fdf56dbef5cacda516b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690871"
---
# <a name="createpatchfileexaw-function"></a>Funzione CreatePatchFileExA/W

Le **funzioni CreatePatchFileExA** e **CreatePatchFileExW** creano un delta tra il file di origine specificato e il file di destinazione specificato. Sia i file di origine che i file di destinazione vengono forniti come percorsi. Anche il delta di output viene scritto in un percorso specificato. Queste funzioni forniscono report sullo stato di avanzamento durante il processo di creazione.

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

Numero totale di file di origine. Usato per creare delta su più file di origine (massimo 255).

*OldFileInfoArray*

Puntatore alla matrice di informazioni sul file di origine.

*NewFileName*

Nome del file di destinazione.

*PatchFileName*

Nome del delta creato.

*Flag di opzione*

Flag di creazione.

*ProgressCallback*

Puntatore al callback di stato definito dall'applicazione.

*CallbackContext*

Puntatore al contesto definito dall'applicazione.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **TRUE** se ha esito positivo; In caso contrario, restituisce **FALSE.**

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| Intestazione | patchapi.h |
| DLL | mspatchc.dll |
| Unicode | Implementato come CreatePatchFileExW (Unicode) e CreatePatchFileExA (ANSI) |

## <a name="see-also"></a>Vedi anche

[PatchAPI](patchapi.md)
