---
description: Definisce un tipo di identificatore univoco globale, in formato Registro di sistema.
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: Tipo semplice GUIDType (contatori delle prestazioni)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 305195784a3578242caefc1fb7eb9bcd8dbd5b557d89d8752bc8242f648abbdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119624921"
---
# <a name="guidtype-simple-type-performance-counters"></a>Tipo semplice GUIDType (contatori delle prestazioni)

Definisce un tipo di identificatore univoco globale, in formato Registro di sistema.

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il **tipo semplice GUIDType** è **un tipo xs:string** limitato dal modello seguente:

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    Il valore deve essere un tipo di identificatore univoco globale in formato Registro di sistema. Ad esempio, {5b2fc63a-8af4-44cb-960c-aefdced908d6}. Usare GUIDGen.exe o UUIDGen.exe per creare un GUID.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 




