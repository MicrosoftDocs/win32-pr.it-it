---
description: Definisce l'elenco delle reti consentite e negate per i computer.
ms.assetid: 21502c97-36a4-4cd6-9dd0-ee44c4cc522f
title: Elemento networkFilter (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkFilter
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d78a23ba1a456f1ad45745fcc25580c27de148c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317121"
---
# <a name="networkfilter-wlanpolicy-element"></a>Elemento networkFilter (WLANPolicy)

L'elemento networkFilter (WLANPolicy) definisce l'elenco delle reti consentite e negate per i computer.

``` syntax
<xs:element name="networkFilter">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="allowList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="network"
                            type="networkItemType"
                            maxOccurs="unbounded"
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
            <xs:element name="blockList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="network"
                            type="networkItemType"
                            maxOccurs="unbounded"
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
            <xs:element name="denyAllIBSS"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="denyAllESS"
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

L'elemento **networkFilter** è definito dall'elemento [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                    | Tipo                                                                     | Descrizione                                                                                    |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**Elenco serializzazione**](wlan-policyschema-allowlist-networkfilter-element.md)     |                                                                          | Elenco di reti LAN wireless a cui deve essere consentita la connessione di qualsiasi computer. <br/> |
| [**blockList**](wlan-policyschema-blocklist-networkfilter-element.md)     |                                                                          | Elenco di reti LAN wireless a cui un computer non deve connettersi.<br/>              |
| [**denyAllESS**](wlan-policyschema-denyalless-networkfilter-element.md)   | boolean                                                                  | Specifica se l'accesso a tutte le reti dell'infrastruttura è bloccato. <br/>                     |
| [**denyAllIBSS**](wlan-policyschema-denyallibss-networkfilter-element.md) | boolean                                                                  | Specifica se l'accesso a tutte le reti ad hoc è bloccato. <br/>                             |
| [**network**](wlan-policyschema-network-allowlist-element.md)             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Rete consentita. <br/>                                                                |
| [**network**](wlan-policyschema-network-blocklist-element.md)             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Rete bloccata. <br/>                                                                 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




