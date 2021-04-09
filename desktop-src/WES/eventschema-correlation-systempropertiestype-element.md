---
title: Elemento Correlation (SystemPropertiesType)
description: Identificatori di attività che possono essere utilizzati dagli utenti per raggruppare gli eventi correlati.
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- EventLog elemento correlazione
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91baca47479fe19988f3bfb23d573b8d92583d79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964669"
---
# <a name="correlation-systempropertiestype-element"></a>Elemento Correlation (SystemPropertiesType)

Identificatori di attività che possono essere utilizzati dagli utenti per raggruppare gli eventi correlati.

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

L'elemento **correlazione** viene definito dal tipo complesso [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Attributi



| Nome              | Tipo                                                | Descrizione                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ActivityID        | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificatore univoco globale che identifica l'attività corrente. Gli eventi pubblicati con questo identificatore fanno parte della stessa attività.<br/>                              |
| RelatedActivityID | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificatore univoco globale che identifica l'attività a cui è stato trasferito il controllo. Gli eventi correlati avrebbero quindi questo identificatore come identificatore ActivityID.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**Sistema (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





