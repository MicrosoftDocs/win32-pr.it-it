---
description: Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione di copia negli Appunti.
title: Funzione DlpNotifyPostCopyToClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: afd054aa0728f3eeb70a5ecbbdeab88460deee2146aa10000665eb56f8d76b65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751850"
---
# <a name="dlpnotifypostcopytoclipboard-function"></a>Funzione DlpNotifyPostCopyToClipboard

Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione di copia negli Appunti.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DocumentInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [struttura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento da cui è stato copiato il contenuto.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ Pollici\]
</dt> <dd>

Puntatore a una [struttura DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenente informazioni sullo stato dell'operazione di copia negli Appunti.

</dd> </dl>


## <a name="return-value"></a>Valore restituito

Restituisce void.

## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |