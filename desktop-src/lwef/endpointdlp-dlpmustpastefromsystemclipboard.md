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
ms.openlocfilehash: 5863173b02cb5c63a2de46653c2d268464e82e65
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495728"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a>Funzione DlpMustPasteFromSystemClipboard

Determina se l'app deve eseguire il pull dei dati dagli Appunti di sistema anziché dalla cache interna.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a>Valore restituito

TRUE se la chiamata negli Appunti del sistema operativo è obbligatoria; in caso contrario, FALSE.

## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |