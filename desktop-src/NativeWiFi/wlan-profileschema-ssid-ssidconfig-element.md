---
description: Contiene un SSID per una LAN wireless.
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: Elemento SSID (SSIDConfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSID
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 644a4afbd10fbfff870007befda964fc9babd593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882674"
---
# <a name="ssid-ssidconfig-element"></a>Elemento SSID (SSIDConfig)

L'elemento SSID (SSIDConfig) contiene un SSID per una LAN wireless.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** In un profilo può essere presente al massimo un elemento **SSID** .

``` syntax
<xs:element name="SSID"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="name"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
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
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L'elemento **SSID** viene definito dall'elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .

## <a name="child-elements"></a>Elementi figlio



| Elemento                                              | Tipo | Descrizione                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [**hex**](wlan-profileschema-hex-ssid-element.md)   |      | Contiene l'SSID di una LAN wireless in formato esadecimale.<br/> |
| [**nome**](wlan-profileschema-name-ssid-element.md) |      | Contiene l'SSID per una LAN wireless.<br/>                      |



## <a name="remarks"></a>Commenti

Anche se gli elementi [**Hex**](wlan-profileschema-hex-ssid-element.md) e [**Name**](wlan-profileschema-name-ssid-element.md) sono facoltativi, è necessario che almeno un elemento **Hex** o [**Name**](wlan-profileschema-name-ssid-element.md) venga visualizzato come figlio dell'elemento **SSID** .

Quando le informazioni sul profilo vengono convertite in un SSID, l'elemento [**Hex**](wlan-profileschema-hex-ssid-element.md) viene convertito nell'SSID (se presente) e l'elemento [**Name**](wlan-profileschema-name-ssid-element.md) viene ignorato. Se l'elemento **esadecimale** non è presente, l'elemento [**Name**](wlan-profileschema-name-ssid-element.md) viene convertito in un SSID mediante la conversione da Unicode a ASCII.

Quando un SSID viene archiviato in un profilo, l'elemento [**esadecimale**](wlan-profileschema-hex-ssid-element.md) viene sempre generato. L'elemento [**Name**](wlan-profileschema-name-ssid-element.md) viene generato solo se la conversione da ASCII a Unicode del SSID e della generazione del profilo XML ha esito positivo. Alcune informazioni provenienti dall'SSID originale potrebbero andare perse quando vengono convertite in un [**nome**](wlan-profileschema-name-ssid-element.md).

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento **SSID** , vedere esempi di profili [wireless](wireless-profile-samples.md).

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

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




