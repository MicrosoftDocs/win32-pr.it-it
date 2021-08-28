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
ms.openlocfilehash: e9e56e25e51a3c6e798242b390f5d8b7341d7306455f1b15eb9e450830d3c9b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064701"
---
# <a name="wlanpolicy-element"></a>Elemento WLANPolicy

**L'elemento WLANPolicy** contiene un criterio LAN wireless. Questo elemento è l'elemento radice univoco per un profilo di criteri wireless.

Lo spazio dei nomi di destinazione per **l'elemento WLANPolicy** è `https://www.microsoft.com/networking/WLAN/policy/v1` .

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
| [**allowEveryoneToCreateAllUserProfiles**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | boolean                                                                  | Specifica se qualsiasi utente può creare un profilo per tutti gli utenti. <br/>                                                               |
| [**allowList**](wlan-policyschema-allowlist-networkfilter-element.md)                                                     |                                                                          | Elenco di reti LAN wireless a cui qualsiasi computer deve essere autorizzato a connettersi. <br/>                                       |
| [**blockList**](wlan-policyschema-blocklist-networkfilter-element.md)                                                     |                                                                          | Elenco di reti LAN wireless a cui un computer non deve connettersi.<br/>                                                    |
| [**denyAllESS**](wlan-policyschema-denyalless-networkfilter-element.md)                                                   | boolean                                                                  | Specifica se l'accesso a tutte le reti dell'infrastruttura è bloccato. <br/>                                                           |
| [**denyAllIBSS**](wlan-policyschema-denyallibss-networkfilter-element.md)                                                 | boolean                                                                  | Specifica se l'accesso a tutte le reti ad hoc è bloccato. <br/>                                                                   |
| [**description**](wlan-policyschema-description-wlanpolicy-element.md)                                                    | [**nameType**](wlan-policyschema-nametype-simpletype.md)                | Descrizione di un criterio LAN wireless. <br/>                                                                                |
| [**enableAutoConfig**](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | boolean                                                                  | Specifica se i computer usano il servizio configurazione automatica (AutoConfig) incorporato per gestire le connessioni wireless. <br/> |
| [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)                                                    |                                                                          | Contiene le impostazioni globali per il modulo di configurazione automatica. <br/>                                                    |
| [**Nome**](wlan-policyschema-name-wlanpolicy-element.md)                                                                  | [**nameType**](wlan-policyschema-nametype-simpletype.md)                | Nome di un criterio LAN wireless. <br/>                                                                                       |
| [**Rete**](wlan-policyschema-network-allowlist-element.md)                                                             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Una rete consentita. <br/>                                                                                                      |
| [**Rete**](wlan-policyschema-network-blocklist-element.md)                                                             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Una rete bloccata. <br/>                                                                                                       |
| [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)                                                |                                                                          | Elenco di reti consentite e negate.<br/>                                                                                  |
| [**profileList**](wlan-policyschema-profilelist-wlanpolicy-element.md)                                                    |                                                                          | Contiene un elenco di profili da applicare a livello di dominio o di computer. <br/>                                                |
| [**showDeniedNetwork**](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | boolean                                                                  | Specifica se le reti negate vengono visualizzate nella **Connessione a una procedura guidata di** rete. <br/>                                         |



## <a name="remarks"></a>Commenti

Per visualizzare l'elenco degli elementi figlio in una struttura ad albero, vedere [Elementi dello schema dei \_ criteri WLAN](wlan-policyschema-elements.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 




