---
title: BITS_FILE_PROPERTY_VALUE struttura (Deliveryoptimization.h)
description: L BITS_FILE_PROPERTY_VALUE union fornisce il valore della proprietà del file DO in base a un valore dell BITS_FILE_PROPERTY_ID enumere.
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- BITS_FILE_PROPERTY_VALUE struttura
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
ms.openlocfilehash: ba01a8c83cef842c40149b3fe8cbc586a7da5f819ffc387befb9f84182cbce24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544626"
---
# <a name="bits_file_property_value-structure"></a>BITS_FILE_PROPERTY_VALUE struttura

**L BITS_FILE_PROPERTY_VALUE** union fornisce il valore della proprietà del file DO in base a un valore [**dell'enumerazione**](bits-file-property-id-.md) BITS_FILE_PROPERTY_ID.

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

Questo valore viene usato quando si usa il valore di enumerazione id **proprietà BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md)
</dt> <dt>

[**IBackgroundCopyFile5.GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[**IBackgroundCopyFile5.SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





