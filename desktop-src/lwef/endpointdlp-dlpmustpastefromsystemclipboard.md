---
description: Determina se l'app deve eseguire il pull dei dati dagli Appunti di sistema anziché dalla cache interna.
title: Funzione DlpMustPasteFromSystemClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpMustPasteFromSystemClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: e111cb85c6eada6f84f7bc10eb240e89447a173e741b26b316b232d742f8de48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888581"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a>Funzione DlpMustPasteFromSystemClipboard

Determina se l'app deve eseguire il pull dei dati dagli Appunti di sistema anziché dalla cache interna.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a>Valore restituito

TRUE se la chiamata negli Appunti del sistema operativo è obbligatoria. in caso contrario, FALSE.

## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |