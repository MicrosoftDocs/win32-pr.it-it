---
description: Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione Incolla dagli Appunti.
title: Funzione DlpNotifyPostPasteFromClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 69a5afbc41350092ebd4d433d2f4d7259ece82cf
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495663"
---
# <a name="dlpnotifypostpastefromclipboard-function"></a>Funzione DlpNotifyPostPasteFromClipboard

Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione Incolla dagli Appunti.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DocumentInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [struttura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento in cui è stato copiato il contenuto.

</dd> </dl>

<dl> <dt>

*Stato operativo* \[ Pollici\]
</dt> <dd>

Puntatore a una struttura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenente informazioni sullo stato relative all'operazione Incolla dagli Appunti.

</dd> </dl>


## <a name="return-value"></a>Valore restituito

Restituisce void.

## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |