---
description: Specifica se un utente può creare un profilo per tutti gli utenti.
ms.assetid: b9bdfe85-b9d5-4dcc-a7f8-05cce9702ec3
title: Elemento allowEveryoneToCreateAllUserProfiles (globalFlags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowEveryoneToCreateAllUserProfiles
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 63bc4c76ccecd8c7f774dc0e73621ef3f9b19877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525765"
---
# <a name="alloweveryonetocreatealluserprofiles-globalflags-element"></a>Elemento allowEveryoneToCreateAllUserProfiles (globalFlags)

L'elemento **allowEveryoneToCreateAllUserProfiles** (globalFlags) specifica se un utente può creare un profilo per tutti gli utenti. Un profilo utente tutti può essere usato da qualsiasi utente nel computer per connettersi alla rete wireless associata al profilo.

Se **allowEveryoneToCreateAllUserProfiles** è true, qualsiasi utente può creare un profilo per tutti gli utenti. Se **allowEveryoneToCreateAllUserProfiles** è false, non tutti gli utenti possono creare un profilo per tutti gli utenti ed è disponibile un DACL associato all'oggetto di \_ \_ sicurezza Aggiungi \_ nuovo tutti i profili utente di WLAN Secure, \_ \_ \_ che specifica gli utenti o i gruppi di utenti con l'autorizzazione per la creazione di tutti i profili utente. Il DACL predefinito specifica che solo gli utenti che hanno eseguito l'accesso come membro del gruppo Administrators possono creare un profilo per tutti gli utenti. Le impostazioni di sicurezza predefinite possono essere modificate chiamando [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings). Per ottenere le impostazioni di sicurezza correnti, chiamare [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).

Questo elemento è obbligatorio. Quando un profilo viene creato dal servizio di configurazione automatica, questo elemento avrà il valore predefinito TRUE.

``` syntax
<xs:element name="allowEveryoneToCreateAllUserProfiles"
    type="boolean"
 />
```

L'elemento **allowEveryoneToCreateAllUserProfiles** è definito dall'elemento [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




