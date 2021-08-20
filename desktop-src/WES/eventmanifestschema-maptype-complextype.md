---
title: Tipo complesso MapType
description: Definisce un elenco di coppie nome/valore.
ms.assetid: 208ae219-8f79-4049-b946-a57b33c97b1b
keywords:
- EventLog di tipo complesso MapType
topic_type:
- apiref
api_name:
- MapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 162676ab5d017c8fa6d6d280a07d1e4500e77cc79e0eacf25e23d5f20c0b3326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120919"
---
# <a name="maptype-complex-type"></a>Tipo complesso MapType

Definisce un elenco di coppie nome/valore.

``` syntax
<xs:complexType name="MapType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="valueMap"
            type="ValueMapType"
         />
        <xs:element name="bitMap"
            type="BitMapType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                          | Tipo                                                                 | Descrizione                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**Bitmap**](eventmanifestschema-bitmap-maptype-element.md)     | [**BitMapType**](eventmanifestschema-bitmaptype-complextype.md)     | Definisce un elenco di coppie nome/valore per il mapping di valori di bit e valori stringa.<br/>     |
| [**valueMap**](eventmanifestschema-valuemap-maptype-element.md) | [**ValueMapType**](eventmanifestschema-valuemaptype-complextype.md) | Definisce un elenco di coppie nome/valore per il mapping di valori interi e valori stringa.<br/> |



## <a name="remarks"></a>Commenti

In genere, si creano mappe per fornire valori stringa enumerati per i dati degli eventi.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come specificare una mappa valori e una bitmap.


```XML
<maps>
   <valueMap name="MyValueMap">
       <map value="5" message="$(string.value5)"/>
       <map value="45" message="$(string.value45)"/>
   </valueMap>
 
   <bitMap name="MyBitmap">
       <map value="0x8" message="$(string.bit3)/>
       <map value="0x80" message="$(string.bit7)/>
   </bitMap>
</maps>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





