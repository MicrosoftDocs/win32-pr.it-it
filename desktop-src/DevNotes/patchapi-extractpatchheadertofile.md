---
description: Estrae le informazioni di intestazione da un Delta.
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
ms.openlocfilehash: 40835a0b88558046ff9086ffcd7ec4609d1ed863
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327844"
---
# <a name="extractpatchheadertofileaw-function"></a>Funzione ExtractPatchHeaderToFileA/W

Le funzioni **ExtractPatchHeaderToFileA** e **ExtractPatchHeaderToFileW** estraggono le informazioni di intestazione da un Delta. Il Delta viene fornito come percorso di file. L'intestazione di output viene scritta anche in un percorso specificato.

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

Nome del Delta che contiene l'intestazione.

*PatchHeaderFileName*

Nome del file di intestazione da creare.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| Intestazione | PatchAPI. h |
| DLL | mspatchc.dll |
| Unicode | Implementato come ExtractPatchHeaderToFileW (Unicode) e ExtractPatchHeaderToFileA (ANSI) |

## <a name="see-also"></a>Vedi anche

[PatchAPI](patchapi.md)
