---
description: Contiene diverse impostazioni per i fornitori di hardware indipendenti.
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
ms.openlocfilehash: d2d2902522c84ebe2939d42301a491521ac8a70f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308883"
---
# <a name="ihv-wlanprofile-element"></a>Elemento IHV (WLANProfile)

L'elemento IHV (WLANProfile) contiene diverse impostazioni per i fornitori di hardware indipendenti. Se un profilo include le impostazioni di sicurezza di IHV, viene eseguito l'override di qualsiasi sicurezza definita da Microsoft.

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

L'elemento è definito dall'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                             | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**connettività**](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | Contiene le impostazioni di connettività correlate a IHV.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**OUI**](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | Contiene un hexBinary di 3 byte che identifica IHV.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | Identifica IHV.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**sicurezza**](wlan-profileschema-security-ihv-element.md)         |                                                                   | Contiene le impostazioni di sicurezza specifiche di IHV. Le impostazioni di sicurezza di Microsoft e le impostazioni di sicurezza di IHV si escludono a vicenda. L'intero profilo non è valido se sono presenti entrambe le impostazioni di sicurezza.<br/>                                                                                                                                                                                            |
| [**tipo**](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | Contiene un hexBinary di 1 byte usato per distinguere le schede di rete con lo stesso IHV.<br/>                                                                                                                                                                                                                                                                                                        |
| [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md)       | [boolean](/dotnet/api/system.boolean) | Specifica l'origine delle impostazioni di sicurezza 802.1 X utilizzate da un componente di sicurezza IHV. Quando [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) è true, i componenti di sicurezza di IHV utilizzano le impostazioni 802.1 x definite da Microsoft. Quando **useMSOneX** è false, i componenti di sicurezza di IHV utilizzano le impostazioni 802.1 x fornite dal fornitore. Per impostazione predefinita, **useMSOneX** è false. Questo elemento è facoltativo.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



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

 

 
