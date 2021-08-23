---
description: Contiene l'SSID di una lan wireless in formato esadecimale.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: Elemento hex (SSID)
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
ms.openlocfilehash: 666562f7a476505dbb0ff23d5354e0f073505d9dd5195bcae17543294cc5f176
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799891"
---
# <a name="hex-ssid-element"></a>Elemento hex (SSID)

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

L'elemento è definito [**dall'elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)

## <a name="remarks"></a>Commenti

Anche se **gli elementi hex** [**e name**](wlan-profileschema-name-ssid-element.md) sono facoltativi, almeno un elemento **hex** o [**name**](wlan-profileschema-name-ssid-element.md) deve essere visualizzato come figlio dell'elemento [**SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)

Quando le informazioni sul profilo vengono convertite in un SSID, l'elemento **esadecimale** viene convertito in SSID (se presente) e l'elemento [**name**](wlan-profileschema-name-ssid-element.md) viene ignorato. Se **l'elemento esadecimale** non è presente, l'elemento [**name**](wlan-profileschema-name-ssid-element.md) viene convertito in un SSID usando la conversione da Unicode a ASCII.

Quando un SSID viene archiviato in un profilo, **l'elemento esadecimale** viene sempre generato. [**L'elemento**](wlan-profileschema-name-ssid-element.md) name viene generato solo se la conversione da ASCII a Unicode di SSID e la generazione del profilo XML hanno esito positivo. Alcune informazioni dell'SSID originale potrebbero andare perse quando vengono convertite in un [**nome**](wlan-profileschema-name-ssid-element.md).

## <a name="examples"></a>Esempio

Per visualizzare un profilo di esempio che usa **l'elemento hex,** vedere [Esempio di profilo FIPS](fips-profile-sample.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP3 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Ssid**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




