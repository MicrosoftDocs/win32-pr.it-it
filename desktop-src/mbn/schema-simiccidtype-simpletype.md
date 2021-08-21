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
ms.openlocfilehash: 33a984875e1e6840787d81dc53c8fc13ead54a0328f6610d75c30075066c13c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035759"
---
# <a name="simiccidtype-simple-type"></a>Tipo semplice simIccIDType

Il **tipo semplice simIccIDType** definisce un tipo per [**l'elemento SimIccID**](schema-simiccid-mbnprofile-element.md) del profilo Mobile Broadband. Questo tipo è una raccolta di cifre e/o lettere maiuscole e minuscole, con una lunghezza di almeno un carattere e al massimo 20 caratteri.

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

Il **tipo semplice simIccIDType** è un token limitato dal modello seguente:

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



 

 




