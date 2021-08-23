---
description: Specifica informazioni sullo stato di un'operazione DLP dell'endpoint.
title: DLP_POSTOP_STATUS struttura (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_POSTOP_STATUS
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 6b8922bee5fb93ee4412833418a63c19dd311c8809cf64132a0f28fbe91d11bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610231"
---
# <a name="dlp_postop_status-structure"></a>DLP_POSTOP_STATUS struttura

Specifica informazioni sullo stato di un'operazione DLP dell'endpoint.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DLP_POSTOP_STATUS {
    
    DWORD Version;    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS; 
```


## <a name="members"></a>Members

<dl> <dt>

*Versione* \[ Pollici\]
</dt> <dd>

Valore DWORD che specifica la versione dell'API. Questo valore deve essere sempre **DLP_POSTOP_STATUS_V_LATEST**. Questa costante è definita nel file di intestazione di esempio endpointdlp.h nell'articolo [Prevenzione della perdita di dati dell'endpoint](endpointdlp-endpoint-data-loss-prevention.md)

</dd> </dl>

<dl> <dt>

*OperationSuccess* \[ Pollici\]
</dt> <dd>

VALORE BOOL che indica se l'operazione di apertura è stata completata correttamente.

</dd> </dl>





## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
