---
title: Snego
description: Snego, il cui identificatore del servizio di autenticazione è RPC \_ C \_ AuthN \_ GSS \_ Negotiate, non fornisce effettivamente i servizi di autenticazione.
ms.assetid: 2087a84c-d302-4511-9f02-2d20ee9e0d8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676b6428d6b7e79893214c2d234dcfc43992e190
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399760"
---
# <a name="snego"></a>Snego

Snego, il cui identificatore del servizio di autenticazione è RPC \_ C \_ AuthN \_ GSS \_ Negotiate, non fornisce effettivamente i servizi di autenticazione. Accetta invece un elenco di servizi di autenticazione e negozia un servizio che funzionerà tra il client e il server. I parametri di autenticazione non vengono usati da Snego, ma vengono passati al servizio di autenticazione scelto, che esegue l'autenticazione effettiva. Snego è stato standardizzato da Internet Engineering Task Force (IETF) nel dicembre 1998, nel documento [RFC 2478](https://www.ietf.org/rfc/rfc2478.txt).

Snego è utile quando non si conoscono i servizi di autenticazione che il computer remoto è in grado di fornire.

Per usare Snego, sia il client che il server devono specificare Snego come servizio di autenticazione. Il server specifica la \_ \_ negoziazione GSS C autenticazione RPC \_ \_ come membro **dwAuthnSvc** di una delle sole strutture [**del \_ \_ servizio di autenticazione**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) nel parametro di matrice *asAuthSvc* passato a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Il client può specificare Snego chiamando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) e passando \_ \_ \_ la negoziazione GSS C AuthN GSS \_ come parametro *dwAuthnSvc* . Il client deve inoltre fornire un elenco di possibili servizi di autenticazione per Snego tramite il membro **Package** list della struttura dell' [**\_ \_ \_ identità \_ di autenticazione WinNT sec**](/windows/desktop/api/sspi/ns-sspi-_sec_winnt_auth_identity_exa) passata al parametro *pAuthInfo* nella chiamata a **CoSetProxyBlanket**. Se *pAuthInfo* è **null**, Snego compone un elenco di servizi di autenticazione dai pacchetti di sicurezza installati nel computer. Quindi Snego invia l'elenco dei servizi di autenticazione al server, confronta l'elenco con i servizi di autenticazione disponibili del server e sceglie un servizio di autenticazione da usare per la connessione.

> [!Note]  
> Schannel non può trovarsi nell'elenco dei servizi di autenticazione utilizzati da Snego.

 

I client possono inoltre specificare Snego quando chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). I parametri *dwAuthnSvc* e *pAuthInfo* di [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) diventano membri di una struttura di [**\_ \_ informazioni di autenticazione unica**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) che viene passata a **CoInitializeSecurity** tramite il parametro *pAuthList* . I dettagli dei valori di tali membri sono gli stessi descritti nel paragrafo precedente.

Se si utilizza Snego, le chiamate a [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket) o [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) restituiranno Snego come servizio di autenticazione, anziché il servizio di autenticazione effettivo che Snego selezionato per stabilire la connessione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pacchetti COM e di sicurezza](com-and-security-packages.md)
</dt> </dl>

 

 