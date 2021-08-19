---
title: Elemento Correlation (SystemPropertiesType)
description: Identificatori di attività che i consumer possono usare per raggruppare gli eventi correlati.
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- Elemento Di correlazione EventLog
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc301c43bbc8ba834949ae2a5056fb4359b5c8db3125da3d1729b18ac7aa1b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120359"
---
# <a name="correlation-systempropertiestype-element"></a>Elemento Correlation (SystemPropertiesType)

Identificatori di attività che i consumer possono usare per raggruppare gli eventi correlati.

``` syntax
<xs:element name="Correlation">
    <xs:complexType>
        <xs:attribute name="ActivityID"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="RelatedActivityID"
            type="GUIDType"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

**L'elemento Correlation** è definito dal tipo complesso [**SystemPropertiesType.**](eventschema-systempropertiestype-complextype.md)

## <a name="attributes"></a>Attributi



| Nome              | Tipo                                                | Descrizione                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ActivityID        | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificatore univoco globale che identifica l'attività corrente. Gli eventi pubblicati con questo identificatore fanno parte della stessa attività.<br/>                              |
| RelatedActivityID | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificatore univoco globale che identifica l'attività a cui è stato trasferito il controllo. Gli eventi correlati avrebbero quindi questo identificatore come identificatore ActivityID.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**Sistema (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





