---
description: Specifica informazioni su un documento associato a un'operazione DLP dell'endpoint.
title: DLP_DOCUMENT_INFO struttura (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_DOCUMENT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 8aa4b6c961b4e80786e9ada480949245b032750499b38f0deead44f97a2d88fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479764"
---
# <a name="dlp_document_info-structure"></a>DLP_DOCUMENT_INFO struttura

Specifica informazioni su un documento associato a un'operazione DLP dell'endpoint.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DLP_DOCUMENT_INFO {

    DWORD Version;    
    LPCWSTR PersistentFileName;
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;
```


## <a name="members"></a>Members

<dl> <dt>

*Versione* \[ Pollici\]
</dt> <dd>

Valore DWORD che specifica la versione dell'API. Questo valore deve essere sempre **DLP_DOCUMENT_INFO_V_LATEST**. Questa costante è definita nel file di intestazione di esempio endpointdlp.h nell'articolo [Prevenzione della perdita dei dati degli endpoint](endpointdlp-endpoint-data-loss-prevention.md).

</dd> </dl>

<dl> <dt>

*PersistentFileName* \[ Pollici\]
</dt> <dd>

Oggetto LPCWSTR che specifica il percorso originale del documento.

</dd> </dl>

<dl> <dt>

*LocalFileName* \[ Pollici\]
</dt> <dd>

Oggetto LPCWSTR che specifica il percorso del file di backup reale del documento.

</dd> </dl>



## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |

