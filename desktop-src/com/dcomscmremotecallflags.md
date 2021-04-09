---
title: DCOMSCMRemoteCallFlags
description: Controlla il comportamento delle chiamate da Gestione controllo servizi DCOM locale (DCOMSCM) a una DCOMSCM remota.
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- Valore DCOMSCMRemoteCallFlags del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda58975e40ac6ac1633db8aa78f2c7636f9103
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047416"
---
# <a name="dcomscmremotecallflags"></a>DCOMSCMRemoteCallFlags

Controlla il comportamento delle chiamate da Gestione controllo servizi DCOM locale (DCOMSCM) a una DCOMSCM remota.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** .



| Valore | Descrizione                                       |
|-------|---------------------------------------------------|
| 0x1   | **DCOMSCM \_ Activation \_ use \_ All \_ AUTHNSERVICES**  |
| 0x2   | **attivazione di DCOMSCM non \_ \_ consente la \_ chiamata non protetta \_** |
| 0x4   | **DCOMSCM \_ Risolvi \_ use \_ All \_ AUTHNSERVICES**     |
| 0x8   | **DCOMSCM \_ risolvere non \_ consentire una \_ chiamata non sicura \_**    |
| 0x10  | **DCOMSCM \_ ping \_ use \_ Mid \_ AUTHNSERVICE**         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a>DCOMSCM \_ Activation \_ use \_ All \_ AUTHNSERVICES Description

Quando il client invia una richiesta di attivazione che usa le impostazioni di sicurezza predefinite, il DCOMSCM locale usa il servizio di autenticazione Negotiate quando effettua la chiamata RPC di attivazione al DCOMSCM remoto. Se la chiamata ha esito negativo, il DCOMSCM locale rende la chiamata RPC di attivazione con nessuna sicurezza.

**Windows Server 2003 e Windows XP/2000:** Se la chiamata RPC di attivazione che utilizza il servizio di autenticazione Negotiate ha esito negativo, il DCOMSCM locale effettua la chiamata RPC di attivazione utilizzando Kerberos, NTLM o altri provider di sicurezza configurati. Se non funziona alcun provider di sicurezza, il DCOMSCM locale effettua la chiamata RPC di attivazione senza alcuna sicurezza.

Impostando questo flag, è possibile eseguire il DCOMSCM locale in Windows Vista o versione successiva per comportarsi come i sistemi precedenti a vista. Non è consigliabile impostare questo flag a meno che non sia necessario per motivi di compatibilità.

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a>DCOMSCM \_ Activation non \_ consente la descrizione della \_ chiamata non protetta \_

Se l'attivazione di Dcomscm non consente l'impostazione del flag di **\_ \_ \_ \_ chiamata non sicuro** , il Dcomscm locale non esegue una chiamata RPC di attivazione non protetta. Per consentire ai client di effettuare richieste di attivazione con impostazioni di sicurezza non predefinite, specificare la struttura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) quando si esegue la richiesta di attivazione. In questo caso, l' **attivazione di Dcomscm \_ \_ utilizza \_ tutti i \_** flag di chiamata AUTHNSERVICES e Dcomscm che non consentono l'attivazione dei flag di **\_ \_ \_ \_ chiamata non protetti** .

Non è consigliabile impostare questo flag a meno che tutti i client e i server nella rete non siano completamente autenticati.

## <a name="dcomscm_resolve_use_all_authnservices-description"></a>DCOMSCM \_ Risolvi \_ use \_ All \_ AUTHNSERVICES Description

Quando il client esegue l'unmarshalling di un riferimento a un oggetto, il DCOMSCM locale usa il servizio di autenticazione Negotiate durante la chiamata RPC di risoluzione OXID al DCOMSCM remoto. Se la chiamata ha esito negativo, il DCOMSCM locale fa in modo che la chiamata RPC di risoluzione OXID non usi alcuna sicurezza.

**Windows Server 2003 e Windows XP/2000:** Se la chiamata RPC di risoluzione OXID che usa il servizio di autenticazione Negotiate ha esito negativo, il DCOMSCM locale esegue la chiamata RPC di risoluzione OXID usando Kerberos, NTLM o altri provider di sicurezza configurati. Se non funziona alcun provider di sicurezza, il DCOMSCM locale esegue la chiamata RPC di risoluzione OXID senza alcuna sicurezza.

Impostando questo flag, è possibile eseguire il DCOMSCM locale in Windows Vista o versione successiva per comportarsi come i sistemi precedenti a vista. Non è consigliabile impostare questo flag a meno che non sia necessario per motivi di compatibilità.

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a>DCOMSCM \_ risolvere non \_ consentire la descrizione della \_ chiamata non protetta \_

Se è impostata l'opzione **Dcomscm \_ Resolve \_ unallow \_ unsecure \_ Call** flag, il Dcomscm locale non esegue una chiamata RPC di risoluzione OXID non protetta. Inoltre, il DCOMSCM locale non esegue una chiamata RPC ping Garbage Collection. Non è consigliabile impostare questo flag a meno che tutti i client e i server nella rete non siano completamente autenticati.

## <a name="dcomscm_ping_use_mid_authnservice-description"></a>DCOMSCM \_ ping \_ use \_ Mid \_ AUTHNSERVICE Description

Il DCOMSCM locale usa il servizio di autenticazione Negotiate quando effettua la chiamata RPC ping della Garbage Collection al DCOMSCM remoto. Se la chiamata ha esito negativo, il DCOMSCM locale rende la chiamata RPC ping della Garbage Collection che non usa alcuna sicurezza.

**Windows Server 2003 e Windows XP/2000:** Se la chiamata RPC ping della Garbage Collection con il servizio di autenticazione Negotiate ha esito negativo, il DCOMSCM locale rende la chiamata RPC ping Garbage Collection tramite Kerberos, NTLM e altri provider di sicurezza configurati. Se non è disponibile alcun provider di sicurezza, il DCOMSCM locale rende la chiamata RPC ping Garbage Collection usando nessuna sicurezza.

Impostando questo flag, è possibile eseguire il DCOMSCM locale in Windows Vista o versione successiva per comportarsi come i sistemi precedenti a vista. Non è consigliabile impostare **Dcomscm \_ ping \_ use \_ Mid \_ AUTHNSERVICE** flag, a meno che non sia necessario per motivi di compatibilità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione per le connessioni remote](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[EnableDCOM](enabledcom.md)
</dt> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 