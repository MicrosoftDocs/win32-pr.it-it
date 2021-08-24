---
description: Specifica informazioni su un documento associato a un'operazione di stampa DLP dell'endpoint.
title: DLP_PRINT_INFO struttura (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_PRINT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: e55b3dc22c77d85e15499ea0fb2a6634ece044496637c811ae42e4afd632704e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725821"
---
# <a name="dlp_print_info-structure"></a>DLP_PRINT_INFO struttura

Specifica informazioni su un documento associato a un'operazione di stampa DLP dell'endpoint.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DLP_PRINT_INFO {
    DWORD Version;
    LPCWSTR PrinterName;
    LPCWSTR JobName;
    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;
```


## <a name="members"></a>Members

<dl> <dt>

*Versione* \[ Pollici\]
</dt> <dd>

Valore DWORD che specifica la versione dell'API. Questo valore deve essere sempre **DLP_PRINT_INFO_V_LATEST**. Questa costante è definita nel file di intestazione di esempio endpointdlp.h nell'articolo [Prevenzione della perdita dei dati dell'endpoint](endpointdlp-endpoint-data-loss-prevention.md).

</dd> </dl>

<dl> <dt>

*PrinterName* \[ Pollici\]
</dt> <dd>

Oggetto LPCWSTR che identifica la stampante di destinazione.

</dd> </dl>

<dl> <dt>

*JobName* \[ Pollici\]
</dt> <dd>

Oggetto LPCWSTR che specifica il nome del processo di stampa.

</dd> </dl>

<dl> <dt>

*OutputFileName* \[ Pollici\]
</dt> <dd>

Oggetto LPCWSTR che specifica il percorso del file di output durante la stampa in un file.

</dd> </dl>



## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |

