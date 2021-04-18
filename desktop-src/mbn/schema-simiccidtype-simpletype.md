---
description: Definisce un tipo per l'elemento SimIccID del profilo Mobile Broadband.
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: Tipo semplice simIccIDType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 410145e659a4845c9c96aaeb76d522de3e0c7b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307527"
---
# <a name="simiccidtype-simple-type"></a>Tipo semplice simIccIDType

Il tipo semplice **simIccIDType** definisce un tipo per l'elemento [**SimIccID**](schema-simiccid-mbnprofile-element.md) del profilo Mobile Broadband. Questo tipo è una raccolta di cifre e/o lettere maiuscole e minuscole, con una lunghezza di almeno un carattere e un massimo di 20 caratteri.

``` syntax
<xs:simpleType name="simIccIDType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="[a-zA-Z\d]{1,20}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il tipo semplice **simIccIDType** è un token che è limitato dal modello seguente:

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



 

 




