---
title: Tipo complesso networkSettingsType
description: Definisce gli elementi che forniscono le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- Utilità di pianificazione di tipo complesso networkSettingsType
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2a8389b1e1f368bedf03fa38dce9c8e262a401
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964434"
---
# <a name="networksettingstype-complex-type"></a>Tipo complesso networkSettingsType

Definisce gli elementi che forniscono le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete.

``` syntax
<xs:complexType name="networkSettingsType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="Id"
            type="guidType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                              | Tipo                                                        | Descrizione                                                                                 |
|----------------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**ID**](taskschedulerschema-id-networksettingstype-element.md)     | [**guidType**](taskschedulerschema-guidtype-simpletype.md) | Specifica un valore GUID che identifica un profilo di rete. <br/>                       |
| [**Nome**](taskschedulerschema-name-networksettingstype-element.md) | nonEmptyString                                              | Specifica il nome di un profilo di rete. Il nome viene usato a scopo di visualizzazione. <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





