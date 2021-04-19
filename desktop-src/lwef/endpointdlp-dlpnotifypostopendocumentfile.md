---
description: Fornisce al sistema informazioni su un file di documento al termine dell'operazione di apertura.
title: Funzione DlpNotifyPostOpenDocumentFile (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 0aed30cc0eca066b569ad1299392430c4d1adeff
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495687"
---
# <a name="dlpnotifypostopendocumentfile-function"></a>Funzione DlpNotifyPostOpenDocumentFile

Fornisce al sistema informazioni su un file di documento dopo il completamento di un'operazione di apertura.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*DocumentInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento aperto.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ Pollici\]
</dt> <dd>

Puntatore a una struttura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenente informazioni sullo stato dell'operazione di apertura del documento.

</dd> </dl>


## <a name="return-value"></a>Valore restituito

Restituisce void.

## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |