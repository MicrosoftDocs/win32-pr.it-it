---
description: Specifica se la LAN virtuale (VLAN) usata dal dispositivo cambia in base alle credenziali dell'utente.
ms.assetid: 4ac92954-adb2-4b0c-9c4e-81f772ea03ed
title: Elemento userBasedVirtualLan (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- userBasedVirtualLan
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9272f61e7efeaf90ba68b1577af9b0062e507984372f7f09ebdbfc15e4ac6fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064971"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a>Elemento userBasedVirtualLan (singleSignOn)

L'elemento userBasedVirtualLan (singleSignOn) specifica se la LAN virtuale (VLAN) usata dal dispositivo cambia in base alle credenziali dell'utente. Alcuni dispositivi nas (Network Access Server) modificano la VLAN dopo l'autenticazione di un utente. Quando userBasedVirtualLan è TRUE, il NAS può modificare la VLAN di un dispositivo dopo l'autenticazione di un utente.

Questo elemento è facoltativo. Quando userBasedVirtualLan non è specificato in un profilo, viene usato il valore FALSE.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

**L'elemento userBasedVirtualLan** è definito dall'elemento [**singleSignOn.**](onexschema-singlesignon-onex-element.md)

## <a name="remarks"></a>Commenti

Questo parametro può essere impostato dalla riga di comando usando il **comando netsh wlan set profileparameter.** Per altre informazioni, vedere [Comandi Netsh per la rete locale wireless (wlan).](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**singleSignOn**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
