---
description: Fornisce al sistema informazioni sullo stato dopo il completamento di un'operazione di stash degli Appunti.
title: Funzione DlpNotifyPostStashClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 97366a356b960fb8bea87bf552bf98576363663a6ca21de290d4035414fcb904
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751660"
---
# <a name="dlpnotifypoststashclipboard-function"></a>Funzione DlpNotifyPostStashClipboard

Fornisce al sistema informazioni sullo stato dopo il completamento di un'operazione di stash degli Appunti.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Parametri


<dl> <dt>

*OpStatus* \[ Pollici\]
</dt> <dd>

Puntatore a una struttura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenente informazioni sullo stato dell'operazione stash clipboard.

</dd> </dl>


## <a name="return-value"></a>Valore restituito

Restituisce void.

## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |