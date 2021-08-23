---
description: Fornisce al sistema informazioni su un documento dopo l'avvio di un'operazione di stampa.
title: Funzione DlpNotifyPostStartPrint (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 23caba53e754c54bfd717274b5f889ad224a2dc80fbe54fb97f70125c0c74f23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976581"
---
# <a name="dlpnotifypoststartprint-function"></a>Funzione DlpNotifyPostStartPrint

Fornisce al sistema informazioni su un documento dopo l'avvio di un'operazione di stampa.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*DocumentInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [struttura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento associato all'operazione di stampa.

</dd> </dl>

<dl> <dt>

*PrintInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [struttura DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) contenente informazioni sull'operazione di stampa.

</dd> </dl>


## <a name="return-value"></a>Valore restituito

Restituisce void.

## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |