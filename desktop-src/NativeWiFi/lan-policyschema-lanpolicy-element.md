---
description: Contiene un criterio LAN cablata.
ms.assetid: c06bdbc4-4199-4eec-a22f-684745912970
title: Elemento LANPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b424a47405aa8f32276019a85902bd51b173cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314761"
---
# <a name="lanpolicy-element"></a>Elemento LANPolicy

L'elemento LANPolicy contiene un criterio LAN cablata. Questo elemento è l'elemento radice univoco per un profilo di criteri di rete cablata.

Lo spazio dei nomi di destinazione per l'elemento **LANPolicy** è `https://www.microsoft.com/networking/LAN/policy/v1` .

``` syntax
<xs:element name="LANPolicy">
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



| Elemento                                                                           | Tipo                                                     | Descrizione                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Descrizione**](lan-policyschema-description-lanpolicy-element.md)             | [**nameType**](lan-policyschema-nametype-simpletype.md) | Contiene la descrizione di un criterio LAN cablata. <br/>                                                                                                                          |
| [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) | boolean                                                  | Specifica se i computer utilizzano il servizio di configurazione automatica incorporato per gestire le connessioni a reti cablate che richiedono l'autenticazione di livello 2, ad esempio 802.1 X.<br/> |
| [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md)             |                                                          | Contiene le impostazioni globali per la configurazione automatica delle reti cablate. <br/>                                                                                          |
| [**nome**](lan-policyschema-name-lanpolicy-element.md)                           | [**nameType**](lan-policyschema-nametype-simpletype.md) | Contiene il nome di un criterio LAN cablata. <br/>                                                                                                                                 |
| [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md)             |                                                          | Contiene un elenco di profili da applicare a livello di dominio o di computer. <br/>                                                                                                |



## <a name="remarks"></a>Commenti

Per visualizzare l'elenco di elementi figlio in una struttura ad albero, vedere [ \_ elementi dello schema del criterio LAN](lan-policyschema-elements.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




