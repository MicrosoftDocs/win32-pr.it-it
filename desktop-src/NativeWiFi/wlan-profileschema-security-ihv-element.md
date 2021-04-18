---
description: Contiene diverse impostazioni di sicurezza utilizzate dai fornitori di hardware indipendenti.
ms.assetid: 237c5d98-3f3c-4279-b2ad-b0d05df041f9
title: Security (IHV)-elemento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ace1bb0ca31f40fdc9d10fba13832797d8d4306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313323"
---
# <a name="security-ihv-element"></a>Security (IHV)-elemento

L'elemento Security (IHV) contiene diverse impostazioni di sicurezza utilizzate dai fornitori di hardware indipendenti.

Le impostazioni di sicurezza di Microsoft e le impostazioni di sicurezza di IHV si escludono a vicenda. Se entrambi i set di impostazioni di sicurezza sono presenti nello stesso profilo, il profilo non è valido.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L'elemento **Security** è definito dall'elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




