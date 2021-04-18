---
title: Struttura BITS_FILE_PROPERTY_VALUE (Deliveryoptimization. h)
description: Il BITS_FILE_PROPERTY_VALUE Unione fornisce il valore della proprietà del file DO in base a un valore dell'enumerazione BITS_FILE_PROPERTY_ID.
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- Struttura BITS_FILE_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 639ea0523c5b92d9764671cb573497223ef968fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301090"
---
# <a name="bits_file_property_value-structure"></a>Struttura BITS_FILE_PROPERTY_VALUE

Il **BITS_FILE_PROPERTY_VALUE** Unione fornisce il valore della proprietà del file do in base a un valore dell'enumerazione [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  LPWSTR String;
} BITS_FILE_PROPERTY_VALUE;
```



## <a name="members"></a>Members

<dl> <dt>

**Stringa**
</dt> <dd>

Questo valore viene usato quando si usa il valore enum di ID proprietà **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md)
</dt> <dt>

[**IBackgroundCopyFile5. GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[**IBackgroundCopyFile5. SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





