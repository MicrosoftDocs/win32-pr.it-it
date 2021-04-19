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
ms.openlocfilehash: 7bc2505b44797edc836ed8ae89e5d9caf3f93f05
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495652"
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