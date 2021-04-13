---
title: Elemento EventRecordID (SystemPropertiesType)
description: Numero di record assegnato all'evento quando è stato registrato.
ms.assetid: d042de4d-e532-432e-bba2-1876a26860a4
keywords:
- EventLog elemento EventRecordID
topic_type:
- apiref
api_name:
- EventRecordID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cb937d075bc0ff5fc1cf8bf1335d1274aee4fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400299"
---
# <a name="eventrecordid-systempropertiestype-element"></a>Elemento EventRecordID (SystemPropertiesType)

Numero di record assegnato all'evento quando è stato registrato.

``` syntax
<xs:element name="EventRecordID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedLong"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

L'elemento **EventRecordID** è definito dal tipo complesso [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





