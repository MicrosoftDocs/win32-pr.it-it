---
description: Contiene uno o più SSID per le reti LAN wireless.
ms.assetid: f9c46db8-2933-48e1-8cb3-effeb13c43ed
title: Elemento SSIDConfig (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSIDConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5665b385c3264ff9d36e79ad671c8f9e8377d4bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882382"
---
# <a name="ssidconfig-wlanprofile-element"></a>Elemento SSIDConfig (WLANProfile)

L'elemento SSIDConfig (WLANProfile) contiene uno o più SSID per le reti LAN wireless.

``` syntax
<xs:element name="SSIDConfig"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="nonBroadcast"
                type="boolean"
                minOccurs="0"
             />
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

L'elemento **SSIDConfig** è definito dall'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                    | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**hex**](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | Contiene l'SSID di una LAN wireless in formato esadecimale.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**nome**](wlan-profileschema-name-ssid-element.md)                       |                                                                   | Contiene il nome del SSID di una LAN senza fili (maiuscole/minuscole).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**nonBroadcast**](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [boolean](/dotnet/api/system.boolean) | Indica se la rete trasmette il relativo SSID.<br/> Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) è impostato su ESS, questo valore può essere **true** o **false**. Il valore predefinito è **true** se questo elemento è assente.<br/> Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) è impostato su IBSS, questo valore deve essere **false**.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/> |
| [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | Contiene un SSID per una LAN wireless.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** In un profilo può essere presente al massimo un elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .<br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento **SSIDConfig** , vedere esempi di profili [wireless](wireless-profile-samples.md).

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
