---
description: Indica se la connessione a una LAN wireless deve essere automatica o avviata dall'utente.
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
ms.openlocfilehash: 3dafb9561bf8b5e3c5c66eb23bd5e286cbd38118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753754"
---
# <a name="connectionmode-wlanprofile-element"></a>Elemento connectionMode (WLANProfile)

L'elemento connectionMode (WLANProfile) indica se la connessione a una LAN wireless deve essere automatica o avviata dall'utente.

Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) è impostato su ESS, questo valore può essere automatico o manuale. Se questo elemento è assente, il valore predefinito è auto.

Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) è impostato su IBSS, questo valore deve essere manuale.

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

L'elemento **ConnectionMode** è definito dall'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="remarks"></a>Commenti

Nella tabella seguente vengono descritti i valori di enumerazione.



| Valore  | Descrizione                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| auto   | La connessione alla rete wireless deve essere avviata automaticamente ogni volta che la rete è compresa nell'intervallo. |
| manual | La connessione alla rete wireless è avviate da solo sulla richiesta esplicita di un utente.               |



 

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento **ConnectionMode** , vedere esempi di profili [wireless](wireless-profile-samples.md).

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

 

 




