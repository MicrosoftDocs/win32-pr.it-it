---
title: Tipo semplice GUIDType (schema eventi)
description: Definisce un tipo di identificatore univoco globale, in formato Registro di sistema. | Tipo semplice GUIDType (schema eventi)
ms.assetid: dbc305ef-6f07-4a70-9013-b89ccec889ea
keywords:
- GuidType tipo semplice EventLog
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2fb7c0cd759b8b58b0db801819ed365f5b25fdb5abdcf886430e8bb2582cbde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750623"
---
# <a name="guidtype-simple-type-event-schema"></a>Tipo semplice GUIDType (schema eventi)

Definisce un tipo di identificatore univoco globale, in formato Registro di sistema.

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il **tipo semplice GUIDType** è una stringa limitata dal modello seguente:

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    Il valore deve essere un tipo di identificatore univoco globale in formato Registro di sistema. Ad esempio, {5b2fc63a-8af4-44cb-960c-aefdced908d6}. Usare GUIDGen.exe o UUIDGen.exe per creare un GUID.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





