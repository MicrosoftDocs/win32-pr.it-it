---
description: Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di stash clipboard.
title: Funzione DlpNotifyPreStashClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 72ecabb2bbfb7517b52790c0d3b7c1ab8075dbd0
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495575"
---
# <a name="dlpnotifyprestashclipboard-function"></a>Funzione DlpNotifyPreStashClipboard

Notifica al sistema prima che venga avviata un'operazione di stash clipboard.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI DlpNotifyPreStashClipboard();
```



## <a name="parameters"></a>Parametri




## <a name="return-value"></a>Valore restituito

Restituisce void.

## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |