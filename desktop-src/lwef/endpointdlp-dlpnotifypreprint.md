---
description: Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di stampa.
title: Funzione DlpNotifyPrePrint (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 1cf0ef44031677495d9b9bedf990877ee931cae245b217faa4225b334df1b3b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479442"
---
# <a name="dlpnotifypreprint-function"></a>Funzione DlpNotifyPrePrint

Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di stampa.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DocumentInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento da stampare.

</dd> </dl>

<dl> <dt>

*PrintInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una struttura [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) contenente informazioni sull'operazione di stampa.

</dd> </dl>


## <a name="return-value"></a>Valore restituito

Restituisce void.

## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |