---
title: Tipo semplice versionType
description: Definisce un modello che specifica una versione di un'attività.
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- Utilità di pianificazione di tipo semplice versionType
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df7010c6ecba29ad0ade80ce403018dd626d01cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340483"
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

Il tipo semplice **versionType** è una **stringa** limitata dal modello seguente:

-   `\d+(\.\d+){1,3}`

    Double seguito da uno, due o tre valori Double. Ad esempio, 1,2 o 1.2.3.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





