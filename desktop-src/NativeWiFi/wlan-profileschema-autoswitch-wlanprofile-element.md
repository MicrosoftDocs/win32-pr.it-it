---
description: Determina il comportamento di roaming di una rete connessa automaticamente quando una rete più preferita è compresa nell'intervallo.
ms.assetid: 095dc797-1249-43aa-a8b7-5fa6eaee2a74
title: Elemento autoswitch (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- autoSwitch
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7ae05b18f58927e05c952edbbfc1b6a6190cec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879990"
---
# <a name="autoswitch-wlanprofile-element"></a>Elemento autoswitch (WLANProfile)

L'elemento autoswitch (WLANProfile) determina il comportamento di roaming di una rete connessa automaticamente quando una rete più preferita è compresa nell'intervallo. . Questo elemento è facoltativo.

Se autoswitch è "true" e [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) è impostato su "auto", è necessario tentare una connessione a una rete più preferita ogni volta che una rete preferita entra in campo. Una rete più preferita è quella che viene ordinata più in alto nell'elenco delle reti wireless preferite. Questo tentativo di connessione viene eseguito quando si è connessi a un'altra rete.

Se [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) è impostato su "auto", questo valore può essere "true" o "false".

Se [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) è impostato su "Manual", questo valore deve essere impostato su "false". Questo elemento non ha alcun effetto su una rete connessa manualmente.

Un valore di autoswitch impostato su "true" comporta una frequenza maggiore di analisi periodica per le nuove reti. Questo può comportare un aumento dell'inquinamento della frequenza radio da queste analisi periodiche e un maggiore consumo di energia usato dalla scheda di rete wireless.

**Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato:** Le modifiche sono implementate in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato per ottimizzare le prestazioni di rete wireless. Queste modifiche sono progettate per ridurre l'inquinamento della frequenza radio, il consumo di energia e l'interruzione del traffico in tempo reale su reti wireless. L'impostazione predefinita per il **commutatore autoswitch** quando questo elemento non è impostato in un profilo LAN wireless è cambiata. L'impostazione predefinita viene modificata in "false" in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato. L'impostazione predefinita è "true" in Windows Server 2008 e Windows Vista. È consigliabile che il valore dell'elemento **autoswitch** utilizzato da un'applicazione in un profilo LAN wireless sia impostato su "false" per ridurre la frequenza di analisi periodica per le nuove reti, a meno che non sia assolutamente necessario che un'applicazione imposti questo valore su "true".

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.

``` syntax
<xs:element name="autoSwitch"
    type="boolean"
 />
```

L'elemento **autoswitch** viene definito dall'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento **autoswitch** , vedere esempi di profili [wireless](wireless-profile-samples.md).

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

 

 




