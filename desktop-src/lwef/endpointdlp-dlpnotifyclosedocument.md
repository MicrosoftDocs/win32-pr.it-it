---
description: Fornisce al sistema informazioni su un documento prima dell'avvio dell'operazione di chiusura del documento.
title: Funzione DlpNotifyCloseDocument (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyCloseDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 06c2b2527833b498ab2b7f5f3fa0f5a662fe67d7
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495722"
---
# <a name="dlpnotifyclosedocument-function"></a>Funzione DlpNotifyCloseDocument

Fornisce al sistema informazioni su un documento prima dell'avvio dell'operazione di chiusura del documento.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DocumentInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento da aprire.

</dd> </dl>


## <a name="return-value"></a>Valore restituito

Restituisce void.

## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |