---
title: DCOMSCMRemoteCallFlags
description: Controlla il comportamento delle chiamate da DCOM Service Control Manager (DCOMSCM) locale a un DCOMSCM remoto.
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- Valore del Registro di sistema DCOMSCMRemoteCallFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d658b80d347e684aa42aebad936a863b9bca2138b3118508849a730e11878d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678831"
---
# <a name="dcomscmremotecallflags"></a>DCOMSCMRemoteCallFlags

Controlla il comportamento delle chiamate da DCOM Service Control Manager (DCOMSCM) locale a un DCOMSCM remoto.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ DWORD REG.**



| Valore | Descrizione                                       |
|-------|---------------------------------------------------|
| 0x1   | **L'ATTIVAZIONE DI DCOMSCM \_ \_ USA TUTTI GLI \_ \_ AUTHNSERVICES**  |
| 0x2   | **L'ATTIVAZIONE DI DCOMSCM \_ NON CONSENTE LA CHIAMATA NON \_ \_ \_ SICURA** |
| 0x4   | **DCOMSCM \_ RESOLVE \_ USE \_ ALL \_ AUTHNSERVICES**     |
| 0x8   | **RISOLUZIONE DCOMSCM \_ NON CONSENTIRE CHIAMATE NON \_ \_ \_ SICURE**    |
| 0x10  | **DCOMSCM \_ PING \_ USE \_ MID \_ AUTHNSERVICE**         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a>DESCRIZIONE DELL'ATTIVAZIONE DI DCOMSCM \_ \_ USE ALL \_ \_ AUTHNSERVICES

Quando il client esegue una richiesta di attivazione che usa le impostazioni di sicurezza predefinite, DCOMSCM locale usa il servizio di autenticazione Negotiate quando effettua la chiamata RPC di attivazione a DCOMSCM remoto. Se la chiamata ha esito negativo, DCOMSCM locale effettua la chiamata RPC di attivazione senza alcuna sicurezza.

**Windows Server 2003 e Windows XP/2000:** Se la chiamata RPC di attivazione che usa il servizio di autenticazione Negotiate ha esito negativo, DCOMSCM locale effettua la chiamata RPC di attivazione usando Kerberos, NTLM o altri provider di sicurezza configurati. Se nessun provider di sicurezza funziona, DCOMSCM locale effettua la chiamata RPC di attivazione senza alcuna sicurezza.

Impostando questo flag, è possibile fare in modo che DCOMSCM locale Windows Vista o versione successiva si comporti come sistemi pre-Vista. Non è consigliabile impostare questo flag a meno che non sia necessario per motivi di compatibilità.

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a>DCOMSCM ACTIVATION DISALLOW UNSECURE CALL DESCRIPTION (ATTIVAZIONE DCOMSCM \_ \_ NON CONSENTE LA \_ DESCRIZIONE DELLE CHIAMATE NON \_ SICURE)

Se il flag **DCOMSCM \_ ACTIVATION \_ DISALLOW \_ UNSECURE \_ CALL** è impostato, DCOMSCM locale non effettua una chiamata RPC di attivazione non sicura. Per consentire ai client di effettuare richieste di attivazione con impostazioni di sicurezza non predefinite, specificare la [**struttura COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) quando effettua la richiesta di attivazione. In questo caso, i flag **DCOMSCM \_ ACTIVATION USE ALL \_ \_ \_ AUTHNSERVICES** e **DCOMSCM \_ ACTIVATION \_ DISALLOW \_ UNSECURE \_ CALL** vengono ignorati.

Non è consigliabile impostare questo flag a meno che tutti i client e i server nella rete non siano completamente autenticati.

## <a name="dcomscm_resolve_use_all_authnservices-description"></a>Descrizione DI DCOMSCM \_ RESOLVE \_ USE ALL \_ \_ AUTHNSERVICES

Quando il client esegue l'unmarshaling di un riferimento a un oggetto, DCOMSCM locale usa il servizio di autenticazione Negotiate durante l'esecuzione della chiamata RPC di risoluzione OXID a DCOMSCM remoto. Se la chiamata ha esito negativo, DCOMSCM locale esegue la chiamata RPC di risoluzione OXID senza alcuna sicurezza.

**Windows Server 2003 e Windows XP/2000:** Se la chiamata RPC di risoluzione OXID che usa il servizio di autenticazione Negotiate ha esito negativo, DCOMSCM locale effettua la chiamata RPC di risoluzione OXID usando Kerberos, NTLM o altri provider di sicurezza configurati. Se nessun provider di sicurezza funziona, DCOMSCM locale effettua la chiamata RPC di risoluzione OXID senza alcuna sicurezza.

Impostando questo flag, è possibile fare in modo che DCOMSCM locale Windows Vista o versione successiva si comporti come sistemi pre-Vista. Non è consigliabile impostare questo flag a meno che non sia necessario per motivi di compatibilità.

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a>DCOMSCM \_ RESOLVE \_ DISALLOW \_ UNSECURE \_ CALL Description

Se il flag **DCOMSCM \_ RESOLVE \_ DISALLOW \_ UNSECURE \_ CALL** è impostato, DCOMSCM locale non effettua una chiamata RPC di risoluzione OXID non sicura. Inoltre, DCOMSCM locale non effettua una chiamata RPC Ping di Garbage Collection non protetta. Non è consigliabile impostare questo flag a meno che tutti i client e i server nella rete non siano completamente autenticati.

## <a name="dcomscm_ping_use_mid_authnservice-description"></a>DCOMSCM \_ PING \_ USE \_ MID \_ AUTHNSERVICE Description

DCOMSCM locale usa il servizio di autenticazione Negotiate quando effettua la chiamata RPC Ping di Garbage Collection a DCOMSCM remoto. Se la chiamata ha esito negativo, DCOMSCM locale esegue la chiamata RPC Ping di Garbage Collection senza alcuna sicurezza.

**Windows Server 2003 e Windows XP/2000:** Se la chiamata RPC Ping di Garbage Collection che usa il servizio di autenticazione Negotiate ha esito negativo, DCOMSCM locale esegue la chiamata RPC Ping di Garbage Collection usando Kerberos, NTLM e altri provider di sicurezza configurati. Se nessun provider di sicurezza funziona, DCOMSCM locale esegue la chiamata RPC Ping di Garbage Collection senza alcuna sicurezza.

Impostando questo flag, il DCOMSCM locale in Windows Vista o versioni successive può essere impostato come sistemi pre-Vista. Non è consigliabile impostare il flag **DCOMSCM \_ PING USE MID \_ \_ \_ AUTHNSERVICE,** a meno che non sia necessario per motivi di compatibilità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione per le connessioni remote](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[Enabledcom](enabledcom.md)
</dt> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 