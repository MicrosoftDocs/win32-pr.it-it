---
description: Specifica i membri della struttura NMCOLUMNVARIANT.
ms.assetid: 29363341-f4d3-43c3-a523-45402174cb74
title: Enumerazione NMCOLUMNTYPE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNTYPE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3c88d001ce3ccf1ebfe1e28855ae9df9fca5d327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760124"
---
# <a name="nmcolumntype-enumeration"></a>Enumerazione NMCOLUMNTYPE

L'enumerazione **NMCOLUMNTYPE** specifica i membri della struttura [**NMCOLUMNVARIANT**](nmcolumnvariant.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  NMCOLUMNTYPE_UINT8      = 0,
  NMCOLUMNTYPE_SINT8,
  NMCOLUMNTYPE_UINT16,
  NMCOLUMNTYPE_SINT16,
  NMCOLUMNTYPE_UINT32,
  NMCOLUMNTYPE_SINT32,
  NMCOLUMNTYPE_FLOAT64,
  NMCOLUMNTYPE_FRAME,
  NMCOLUMNTYPE_YESNO,
  NMCOLUMNTYPE_ONOFF,
  NMCOLUMNTYPE_TRUEFALSE,
  NMCOLUMNTYPE_MACADDR,
  NMCOLUMNTYPE_IPXADDR,
  NMCOLUMNTYPE_IPADDR,
  NMCOLUMNTYPE_VARTIME,
  NMCOLUMNTYPE_STRING
} NMCOLUMNTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**\_Uint8 NMCOLUMNTYPE**
</dt> <dd>

Unsigned Integer a 8 bit.

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**\_SINT8 NMCOLUMNTYPE**
</dt> <dd>

intero con segno a 8 bit.

</dd> <dt>

<span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**NMCOLUMNTYPE \_ UInt16**
</dt> <dd>

Unsigned Integer a 16 bit.

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**\_SINT16 NMCOLUMNTYPE**
</dt> <dd>

intero con segno a 16 bit.

</dd> <dt>

<span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**\_UInt32 NMCOLUMNTYPE**
</dt> <dd>

Unsigned Integer a 32 bit.

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**\_SINT32 NMCOLUMNTYPE**
</dt> <dd>

Intero con segno a 32 bit.

</dd> <dt>

<span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**\_FLOAT64 NMCOLUMNTYPE**
</dt> <dd>

float a 64 bit.

</dd> <dt>

<span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**\_frame NMCOLUMNTYPE**
</dt> <dd>

Numero di frame.

</dd> <dt>

<span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**\_YesNo NMCOLUMNTYPE**
</dt> <dd>

"Yes" o "No".

</dd> <dt>

<span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**\_OnOff NMCOLUMNTYPE**
</dt> <dd>

"On" o "off"

</dd> <dt>

<span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**\_TRUEFALSE NMCOLUMNTYPE**
</dt> <dd>

"True" o "false".

</dd> <dt>

<span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**\_MACADDR NMCOLUMNTYPE**
</dt> <dd>

Indirizzo MAC.

</dd> <dt>

<span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**\_IPXADDR NMCOLUMNTYPE**
</dt> <dd>

Indirizzo IPX.

</dd> <dt>

<span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**\_IPADDR NMCOLUMNTYPE**
</dt> <dd>

Un indirizzo IP.

</dd> <dt>

<span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**\_VARTIME NMCOLUMNTYPE**
</dt> <dd>

Tempo Variant.

</dd> <dt>

<span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**\_stringa NMCOLUMNTYPE**
</dt> <dd>

Puntatore a una stringa.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




