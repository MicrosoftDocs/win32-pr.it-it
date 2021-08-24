---
description: Fornisce al sistema informazioni su un documento prima che venga avviata un'operazione Incolla dagli Appunti.
title: Funzione DlpNotifyPrePasteFromClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b490f4f5a258805c785822d815d9e341feb8bbd494e428eb7bf1be6da843d775
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778181"
---
# <a name="dlpnotifyprepastefromclipboard-function"></a>Funzione DlpNotifyPrePasteFromClipboard

Fornisce al sistema informazioni su un documento prima che venga avviata un'operazione Incolla dagli Appunti.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DocumentInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [struttura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento in cui viene incollato il contenuto.

</dd> </dl>




## <a name="return-value"></a>Valore restituito

Restituisce void.

## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |