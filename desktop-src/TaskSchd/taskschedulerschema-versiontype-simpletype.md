---
title: Tipo semplice versionType
description: Definisce un modello che specifica una versione di un'attività.
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- tipo semplice versionType Utilità di pianificazione
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 52ad30f5ea14a447e2a08151ef2803b0577066e147e29673d373ce87eee033f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355037"
---
# <a name="versiontype-simple-type"></a>Tipo semplice versionType

Definisce un modello che specifica una versione di un'attività.

``` syntax
<xs:simpleType name="versionType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\d+(\.\d+){1,3}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il **tipo semplice versionType** è una **stringa** limitata dal modello seguente:

-   `\d+(\.\d+){1,3}`

    Valore double seguito da uno, due o tre valori double. Ad esempio, 1.2 o 1.2.3.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





