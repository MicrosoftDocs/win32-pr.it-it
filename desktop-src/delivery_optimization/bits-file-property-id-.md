---
title: Enumerazione BITS_FILE_PROPERTY_ID (Deliveryoptimization. h)
description: L'enumerazione BITS_FILE_PROPERTY_ID specifica i valori che definiscono i valori ID corrispondenti alle proprietà BackgroundCopyFile.
ms.assetid: 47EFD160-7CA8-48E6-A18E-38D85F7C6E47
keywords:
- Enumerazione BITS_FILE_PROPERTY_ID
- Enumerazione BITS_FILE_PROPERTY_ID
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b6c6b8a4de359e8313e3127080f2cc17ae6478c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301435"
---
# <a name="bits_file_property_id-enumeration"></a>Enumerazione BITS_FILE_PROPERTY_ID

L'enumerazione **BITS_FILE_PROPERTY_ID** specifica i valori che definiscono i valori ID corrispondenti alle proprietà **BackgroundCopyFile** .

## <a name="syntax"></a>Sintassi


```C++
typedef enum _BITS_FILE_PROPERTY_ID { 
  BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS  = 1
} BITS_FILE_PROPERTY_ID;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS"></span><span id="bits_file_property_id_http_response_headers"></span>**BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**
</dt> <dd>

Set completo di intestazioni di risposta HTTP dall'ultimo pacchetto di risposta HTTP del server.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 





