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
ms.openlocfilehash: d588b627a4d5a88162cb0af67df1b5bf4fd943f1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495783"
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

