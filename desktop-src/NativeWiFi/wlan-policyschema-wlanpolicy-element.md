---
description: Contiene un criterio LAN wireless.
ms.assetid: 16ffb682-f88b-4ca1-a902-d2db5e347975
title: Elemento WLANPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ec26a3cab15014deabca4e9332c1fbef7a788b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130434"
---
# <a name="wlanpolicy-element"></a>Elemento WLANPolicy

L'elemento **WLANPolicy** contiene un criterio LAN wireless. Questo elemento è l'elemento radice univoco per un profilo dei criteri wireless.

Lo spazio dei nomi di destinazione per l'elemento **WLANPolicy** è `https://www.microsoft.com/networking/WLAN/policy/v1` .

``` syntax
<xs:element name="WLANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
                         />
                        <xs:element name="showDeniedNetwork"
                            type="boolean"
                         />
                        <xs:element name="allowEveryoneToCreateAllUserProfiles"
                            type="boolean"
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
            <xs:element name="networkFilter"
                minOccurs="0"
            >
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
            <xs:element name="profileList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
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

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                                    | Tipo                                                                     | Descrizione                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**allowEveryoneToCreateAllUserProfiles**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | boolean                                                                  | Specifica se un utente può creare un profilo per tutti gli utenti. <br/>                                                               |
| [**Elenco serializzazione**](wlan-policyschema-allowlist-networkfilter-element.md)                                                     |                                                                          | Elenco di reti LAN wireless a cui deve essere consentita la connessione di qualsiasi computer. <br/>                                       |
| [**blockList**](wlan-policyschema-blocklist-networkfilter-element.md)                                                     |                                                                          | Elenco di reti LAN wireless a cui un computer non deve connettersi.<br/>                                                    |
| [**denyAllESS**](wlan-policyschema-denyalless-networkfilter-element.md)                                                   | boolean                                                                  | Specifica se l'accesso a tutte le reti dell'infrastruttura è bloccato. <br/>                                                           |
| [**denyAllIBSS**](wlan-policyschema-denyallibss-networkfilter-element.md)                                                 | boolean                                                                  | Specifica se l'accesso a tutte le reti ad hoc è bloccato. <br/>                                                                   |
| [**Descrizione**](wlan-policyschema-description-wlanpolicy-element.md)                                                    | [**nameType**](wlan-policyschema-nametype-simpletype.md)                | Descrizione di un criterio LAN wireless. <br/>                                                                                |
| [**enableAutoConfig**](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | boolean                                                                  | Specifica se i computer utilizzano il servizio di configurazione automatica (AutoConfig) incorporato per gestire le connessioni wireless. <br/> |
| [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)                                                    |                                                                          | Contiene le impostazioni globali per il modulo di configurazione automatica (ACM). <br/>                                                    |
| [**nome**](wlan-policyschema-name-wlanpolicy-element.md)                                                                  | [**nameType**](wlan-policyschema-nametype-simpletype.md)                | Nome di un criterio LAN wireless. <br/>                                                                                       |
| [**network**](wlan-policyschema-network-allowlist-element.md)                                                             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Rete consentita. <br/>                                                                                                      |
| [**network**](wlan-policyschema-network-blocklist-element.md)                                                             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Rete bloccata. <br/>                                                                                                       |
| [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)                                                |                                                                          | Elenco di reti consentite e negate.<br/>                                                                                  |
| [**profileList**](wlan-policyschema-profilelist-wlanpolicy-element.md)                                                    |                                                                          | Contiene un elenco di profili da applicare a livello di dominio o di computer. <br/>                                                |
| [**showDeniedNetwork**](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | boolean                                                                  | Specifica se le reti negate vengono visualizzate nella procedura guidata **Connetti a una rete** . <br/>                                         |



## <a name="remarks"></a>Commenti

Per visualizzare l'elenco di elementi figlio in una struttura simile a un albero, [vedere \_ elementi dello schema dei criteri di rete WLAN](wlan-policyschema-elements.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




