---
description: Specifica se la LAN virtuale (VLAN) usata dal dispositivo viene modificata in base alle credenziali dell'utente.
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
ms.openlocfilehash: 6ef421e35f7fa121c31e58cfeba4eee969a1b6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129731"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a>Elemento userBasedVirtualLan (singleSignOn)

L'elemento userBasedVirtualLan (singleSignOn) specifica se la LAN virtuale (VLAN) usata dal dispositivo viene modificata in base alle credenziali dell'utente. Alcuni dispositivi NAS (Network Access Server) modificano la VLAN dopo l'autenticazione dell'utente. Quando userBasedVirtualLan è TRUE, il NAS può modificare la VLAN di un dispositivo dopo l'autenticazione dell'utente.

Questo elemento è facoltativo. Quando userBasedVirtualLan non viene specificato in un profilo, viene usato il valore FALSE.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

L'elemento **userBasedVirtualLan** è definito dall'elemento [**singleSignOn**](onexschema-singlesignon-onex-element.md) .

## <a name="remarks"></a>Commenti

Questo parametro può essere impostato dalla riga di comando tramite il comando **netsh wlan set profileparameter** . Per ulteriori informazioni, vedere [comandi Netsh per WLAN (wireless local area network)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



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

 

 
