---
description: Contiene varie impostazioni per i fornitori di hardware indipendenti.
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: Elemento IHV (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IHV
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1cfcd9ee463ef91d04d0bebbeac800d48da32fdd777edc2a08ccf0051410160d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799921"
---
# <a name="ihv-wlanprofile-element"></a>Elemento IHV (WLANProfile)

L'elemento IHV (WLANProfile) contiene varie impostazioni per i fornitori di hardware indipendenti. Se un profilo include impostazioni di sicurezza IHV, esegue l'override di qualsiasi sicurezza definita da Microsoft.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.

``` syntax
<xs:element name="IHV"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUIHeader">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUI">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="3"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="type">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="1"
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
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="useMSOneX"
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

L'elemento è definito [**dall'elemento WLANProfile.**](wlan-profileschema-wlanprofile-element.md)

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                             | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Connettività**](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | Contiene le impostazioni di connettività correlate a IHV.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**Oui**](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | Contiene un oggetto hexBinary a 3 byte che identifica l'IHV.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | Identifica l'IHV.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**Sicurezza**](wlan-profileschema-security-ihv-element.md)         |                                                                   | Contiene le impostazioni di sicurezza specifiche di IHV. Le impostazioni di sicurezza Microsoft e le impostazioni di sicurezza IHV si escludono a vicenda. L'intero profilo non è valido se sono presenti entrambe le impostazioni di sicurezza.<br/>                                                                                                                                                                                            |
| [**digitare**](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | Contiene un oggetto hexBinary a 1 byte usato per differenziare le schede di interfaccia di rete in base allo stesso IHV.<br/>                                                                                                                                                                                                                                                                                                        |
| [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md)       | [boolean](/dotnet/api/system.boolean) | Specifica l'origine delle impostazioni di sicurezza 802.1X usate da un componente di sicurezza IHV. Quando [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) è true, i componenti di sicurezza IHV usano le impostazioni 802.1X definite da Microsoft. Quando **useMSOneX** è false, i componenti di sicurezza IHV usano le impostazioni 802.1X fornite dal fornitore. Per impostazione predefinita, **useMSOneX** è false. Questo elemento è facoltativo.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
