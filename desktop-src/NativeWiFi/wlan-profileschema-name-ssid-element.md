---
description: Contiene l'SSID di una LAN wireless.
ms.assetid: ed23ccd0-9b44-4c97-a5ed-93e86632b819
title: Elemento Name (SSID)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dbb1301de2a2d70edf8c61de002c28e48b00a5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883922"
---
# <a name="name-ssid-element"></a>Elemento Name (SSID)

L'elemento Name (SSID) contiene il valore SSID di una LAN wireless.

``` syntax
<xs:element name="name">
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
```

L'elemento è definito dall'elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

## <a name="remarks"></a>Commenti

I nomi fanno distinzione tra maiuscole e minuscole.

Anche se gli elementi [**Hex**](wlan-profileschema-hex-ssid-element.md) e **Name** sono facoltativi, è necessario che almeno un elemento **Hex** o **Name** venga visualizzato come figlio dell'elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

Quando le informazioni sul profilo vengono convertite in un SSID, l'elemento [**Hex**](wlan-profileschema-hex-ssid-element.md) viene convertito nell'SSID (se presente) e l'elemento **Name** viene ignorato. Se l'elemento **esadecimale** non è presente, l'elemento **Name** viene convertito in un SSID mediante la conversione da Unicode a ASCII.

Quando un SSID viene archiviato in un profilo, l'elemento [**esadecimale**](wlan-profileschema-hex-ssid-element.md) viene sempre generato. L'elemento **Name** viene generato solo se la conversione da ASCII a Unicode del SSID e della generazione del profilo XML ha esito positivo. Alcune informazioni provenienti dall'SSID originale potrebbero andare perse quando vengono convertite in un **nome**.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** I caratteri di escape XML, ad esempio &, non vengono visualizzati. Evitare di utilizzare caratteri di escape XML nei nomi SSID per i profili distribuiti in Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2.

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento **Name** , vedere esempi di profili [wireless](wireless-profile-samples.md).

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

 

 




