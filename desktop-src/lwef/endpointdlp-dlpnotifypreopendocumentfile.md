---
description: Fornisce al sistema informazioni su un file di documento prima dell'avvio di un'operazione di apertura.
title: Funzione DlpNotifyPreOpenDocumentFile (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: f2be797d0f4045f17e753031247797406f332afa2fcc47b3ca83973527d99216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778231"
---
# <a name="dlpnotifypreopendocumentfile-function"></a>Funzione DlpNotifyPreOpenDocumentFile

Fornisce al sistema informazioni su un file di documento prima dell'avvio di un'operazione di apertura.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
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