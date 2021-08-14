---
title: Tipo complesso networkSettingsType
description: Definisce gli elementi che forniscono le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- Tipo complesso networkSettingsType Utilità di pianificazione
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9969e4e3827d926d8c295d4e1a3ce7b77550804eb4995a267a920a16871837f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758471"
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
| [**Id**](taskschedulerschema-id-networksettingstype-element.md)     | [**guidType**](taskschedulerschema-guidtype-simpletype.md) | Specifica un valore GUID che identifica un profilo di rete. <br/>                       |
| [**Nome**](taskschedulerschema-name-networksettingstype-element.md) | nonEmptyString                                              | Specifica il nome di un profilo di rete. Il nome viene usato a scopo di visualizzazione. <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





