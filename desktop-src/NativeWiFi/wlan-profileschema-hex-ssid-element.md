---
description: Contiene l'SSID di una LAN wireless in formato esadecimale.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: Hex (SSID) (elemento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- hex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6bc214f50788fdc6965a1ce429c5c2919846cf72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307828"
---
# <a name="hex-ssid-element"></a>Hex (SSID) (elemento)

L'elemento esadecimale (SSID) contiene l'SSID di una LAN wireless in formato esadecimale.

``` syntax
<xs:element name="hex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="32"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento è definito dall'elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

## <a name="remarks"></a>Commenti

Anche se gli elementi **Hex** e [**Name**](wlan-profileschema-name-ssid-element.md) sono facoltativi, è necessario che almeno un elemento **Hex** o [**Name**](wlan-profileschema-name-ssid-element.md) venga visualizzato come figlio dell'elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

Quando le informazioni sul profilo vengono convertite in un SSID, l'elemento **Hex** viene convertito nell'SSID (se presente) e l'elemento [**Name**](wlan-profileschema-name-ssid-element.md) viene ignorato. Se l'elemento **esadecimale** non è presente, l'elemento [**Name**](wlan-profileschema-name-ssid-element.md) viene convertito in un SSID mediante la conversione da Unicode a ASCII.

Quando un SSID viene archiviato in un profilo, l'elemento **esadecimale** viene sempre generato. L'elemento [**Name**](wlan-profileschema-name-ssid-element.md) viene generato solo se la conversione da ASCII a Unicode del SSID e della generazione del profilo XML ha esito positivo. Alcune informazioni provenienti dall'SSID originale potrebbero andare perse quando vengono convertite in un [**nome**](wlan-profileschema-name-ssid-element.md).

## <a name="examples"></a>Esempio

Per visualizzare un profilo di esempio che usa l'elemento **esadecimale** , vedere [esempio di profilo FIPS](fips-profile-sample.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




