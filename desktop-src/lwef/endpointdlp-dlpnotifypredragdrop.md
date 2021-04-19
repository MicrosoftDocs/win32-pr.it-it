---
description: Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di trascinamento della selezione.
title: Funzione DlpNotifyPreDragDrop (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreDragDrop
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d88a28c0dff4b13cf1c1848eeb8623c3acd1c024
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495639"
---
# <a name="dlpnotifypredragdrop-function"></a>Funzione DlpNotifyPreDragDrop

Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di trascinamento della selezione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DocumentInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [struttura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento associato all'operazione di trascinamento della selezione.

</dd> </dl>


## <a name="return-value"></a>Valore restituito

Restituisce void.

## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |