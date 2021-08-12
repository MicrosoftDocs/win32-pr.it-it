---
description: Contiene un SSID per una rete LAN wireless.
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
ms.openlocfilehash: 5d58ed866e79269e604fe49ad8afe65d557f27a90d0be03904b8d27da5ac5c2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619058"
---
# <a name="ssid-ssidconfig-element"></a>Elemento SSID (SSIDConfig)

L'elemento SSIDConfig (SSIDConfig) contiene un SSID per una rete LAN wireless.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Al massimo un **elemento SSID** può essere visualizzato in un profilo.

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

**L'elemento SSID** è definito dall'elemento [**SSIDConfig.**](wlan-profileschema-ssidconfig-wlanprofile-element.md)

## <a name="child-elements"></a>Elementi figlio



| Elemento                                              | Tipo | Descrizione                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [**hex**](wlan-profileschema-hex-ssid-element.md)   |      | Contiene l'SSID di una rete LAN wireless in formato esadecimale.<br/> |
| [**Nome**](wlan-profileschema-name-ssid-element.md) |      | Contiene l'SSID per una rete LAN wireless.<br/>                      |



## <a name="remarks"></a>Commenti

Anche se [**gli elementi hex**](wlan-profileschema-hex-ssid-element.md) [**e name**](wlan-profileschema-name-ssid-element.md) sono facoltativi, almeno un elemento **esadecimale** o [**name**](wlan-profileschema-name-ssid-element.md) deve essere visualizzato come figlio dell'elemento **SSID.**

Quando le informazioni sul profilo vengono convertite in un SSID, l'elemento [**esadecimale**](wlan-profileschema-hex-ssid-element.md) viene convertito in SSID (se presente) e l'elemento [**name**](wlan-profileschema-name-ssid-element.md) viene ignorato. Se **l'elemento esadecimale** non è presente, [**l'elemento name**](wlan-profileschema-name-ssid-element.md) viene convertito in un SSID usando la conversione da Unicode a ASCII.

Quando un SSID viene archiviato in un profilo, [**l'elemento esadecimale**](wlan-profileschema-hex-ssid-element.md) viene sempre generato. [**L'elemento**](wlan-profileschema-name-ssid-element.md) name viene generato solo se la conversione da ASCII a Unicode dell'SSID e la generazione del profilo XML hanno esito positivo. Alcune informazioni dell'SSID originale potrebbero andare perse quando vengono convertite in un [**nome**](wlan-profileschema-name-ssid-element.md).

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano **l'elemento SSID,** vedere [Esempi di profili wireless.](wireless-profile-samples.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP3 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




