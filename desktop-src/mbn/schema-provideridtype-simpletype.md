---
description: Definisce un tipo per l'elemento ProviderID del profilo Mobile Broadband.
ms.assetid: 84193749-c98d-4313-bf99-3da1c74d7cc4
title: Tipo semplice providerIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerIdType
api_type:
- Schema
ms.openlocfilehash: ec3c952395be048d18305172e64618fa26313f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129007"
---
# <a name="provideridtype-simple-type"></a>Tipo semplice providerIdType

Il tipo semplice **providerIdType** definisce un tipo per l'elemento [**ProviderID**](schema-providerid-providertype-element.md) del profilo Mobile Broadband. Questo tipo è una raccolta di cifre con una lunghezza di almeno una cifra e un massimo di 6 cifre.

``` syntax
<xs:simpleType name="providerIdType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="\d{1,6}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il tipo semplice **providerIdType** è un token che è limitato dal modello seguente:

-   `\d{1,6}`

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



 

 




