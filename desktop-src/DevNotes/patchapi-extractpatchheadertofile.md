---
description: Estrae le informazioni di intestazione da un delta.
title: Funzione ExtractPatchHeaderToFileA/W
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: ExtractPatchHeaderToFileA, ExtractPatchHeaderToFileW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtractPatchHeaderToFileW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 626bd53e3361f4d29cc76e17ae2788ddea3bc8b99b580196bcbf77c27a6983d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571801"
---
# <a name="extractpatchheadertofileaw-function"></a>Funzione ExtractPatchHeaderToFileA/W

Le **funzioni ExtractPatchHeaderToFileA** **ed ExtractPatchHeaderToFileW** estraggono le informazioni di intestazione da un delta. Il delta viene fornito come percorso di file. Anche l'intestazione di output viene scritta in un percorso specificato.

## <a name="syntax"></a>Sintassi

```cpp
BOOL  PATCHAPI  ExtractPatchHeaderToFileA(
    LPCTSTR  PatchFileName,
    LPCTSTR  PatchHeaderFileName
    );

BOOL  PATCHAPI  ExtractPatchHeaderToFileW(
    LPCWSTR  PatchFileName,
    LPCWSTR  PatchHeaderFileName
    );
```

## <a name="parameters"></a>Parametri

*PatchFileName*

Nome del delta contenente l'intestazione.

*PatchHeaderFileName*

Nome del file di intestazione da creare.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **TRUE** se ha esito positivo. In caso contrario, restituisce **FALSE.**

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| Intestazione | patchapi.h |
| DLL | mspatchc.dll |
| Unicode | Implementato come ExtractPatchHeaderToFileW (Unicode) ed ExtractPatchHeaderToFileA (ANSI) |

## <a name="see-also"></a>Vedi anche

[PatchAPI](patchapi.md)
