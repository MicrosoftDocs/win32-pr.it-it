---
description: Contiene le impostazioni globali per il modulo di configurazione automatica.
ms.assetid: fb2b96d0-38cc-44fe-a82a-97e73b6a8f2a
title: Elemento globalFlags (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2851ae779bf1693d44642f87d33a71c17000e9dc0b68eeb8daab83972b37457d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800331"
---
# <a name="globalflags-wlanpolicy-element"></a>Elemento globalFlags (WLANPolicy)

L'elemento globalFlags (WLANPolicy) contiene le impostazioni globali per il modulo di configurazione automatica . Questo elemento è obbligatorio.

``` syntax
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
```

**L'elemento globalFlags** è definito dall'elemento [**WLANPolicy.**](wlan-policyschema-wlanpolicy-element.md)

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                                    | Tipo    | Descrizione                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**allowEveryoneToCreateAllUserProfiles**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | boolean | Specifica se qualsiasi utente può creare un profilo per tutti gli utenti. <br/>                                                               |
| [**enableAutoConfig**](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | boolean | Specifica se i computer usano il servizio configurazione automatica (AutoConfig) incorporato per gestire le connessioni wireless. <br/> |
| [**showDeniedNetwork**](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | boolean | Specifica se le reti negate vengono visualizzate nella **Connessione a una procedura guidata di** rete. <br/>                                         |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Criteri WLAN**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**Criteri WLAN**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




