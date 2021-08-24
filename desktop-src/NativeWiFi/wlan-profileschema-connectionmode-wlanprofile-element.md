---
description: Indica se la connessione a una rete LAN wireless deve essere automatica o avviata dall'utente.
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: Elemento connectionMode (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a6ef18eff8ba27a3169399f1f10e0707c4e0b3c010d54830ad8f8f997c5e1b50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684441"
---
# <a name="connectionmode-wlanprofile-element"></a>Elemento connectionMode (WLANProfile)

L'elemento connectionMode (WLANProfile) indica se la connessione a una rete LAN wireless deve essere automatica o avviata dall'utente.

Se [**connectionType è**](wlan-profileschema-connectiontype-wlanprofile-element.md) impostato su ESS, questo valore può essere automatico o manuale. Il valore predefinito è auto se questo elemento è assente.

Se [**connectionType è**](wlan-profileschema-connectiontype-wlanprofile-element.md) impostato su IBSS, questo valore deve essere manuale.

``` syntax
<xs:element name="connectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="manual"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**L'elemento connectionMode** è definito dall'elemento [**WLANProfile.**](wlan-profileschema-wlanprofile-element.md)

## <a name="remarks"></a>Commenti

Nella tabella seguente vengono descritti i valori di enumerazione.



| Valore  | Descrizione                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| auto   | La connessione alla rete wireless deve essere avviata automaticamente ogni volta che la rete è in intervallo. |
| manual | La connessione alla rete wireless viene stabilita solo su richiesta esplicita di un utente.               |



 

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano **l'elemento connectionMode,** vedere [Esempi di profili wireless](wireless-profile-samples.md).

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




