---
description: Specifica le informazioni sullo stato di un'operazione DLP dell'endpoint.
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
ms.openlocfilehash: c0221926700fc8960de5ef4d25c36136c3fc9737
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495580"
---
# <a name="dlp_postop_status-structure"></a>DLP_POSTOP_STATUS struttura

Specifica le informazioni sullo stato di un'operazione DLP dell'endpoint.

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

Valore DWORD che specifica la versione dell'API. Questo valore deve essere sempre **DLP_POSTOP_STATUS_V_LATEST**. Questa costante è definita nel file di intestazione di esempio endpointdlp.h nell'articolo [Prevenzione della perdita dei dati degli endpoint](endpointdlp-endpoint-data-loss-prevention.md)

</dd> </dl>

<dl> <dt>

*OperazioneSuccess* \[ Pollici\]
</dt> <dd>

Valore BOOL che indica se l'operazione di apertura è riuscita.

</dd> </dl>





## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
