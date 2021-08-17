---
title: Snego
description: Snego, il cui identificatore del servizio di autenticazione è RPC \_ C \_ AUTHN \_ GSS NEGOTIATE, non fornisce \_ effettivamente i servizi di autenticazione stessi.
ms.assetid: 2087a84c-d302-4511-9f02-2d20ee9e0d8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82f8da58cc77ebfd4debd0763ad4af6e1c96d3e88d9ede69ff82a28e3d8a5ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129813"
---
# <a name="snego"></a>Snego

Snego, il cui identificatore del servizio di autenticazione è RPC \_ C \_ AUTHN \_ GSS NEGOTIATE, non fornisce \_ effettivamente i servizi di autenticazione stessi. Accetta invece un elenco di servizi di autenticazione e negozia un servizio che funzionerà tra il client e il server. I parametri di autenticazione non vengono usati da Snego, ma vengono passati al servizio di autenticazione scelto, che esegue l'autenticazione effettiva. Snego è stato standardizzato dalla Internet Engineering Task Force (IETF) nel dicembre 1998, nel documento [RFC 2478](https://www.ietf.org/rfc/rfc2478.txt).

Snego è utile quando non si conoscono i servizi di autenticazione che il computer remoto può fornire.

Per usare Snego, sia il client che il server devono specificare Snego come servizio di autenticazione. Il server specifica RPC \_ C \_ AUTHN GSS NEGOTIATE come membro \_ \_ **dwAuthnSvc** [**\_ \_**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) di  una delle strutture SOLE AUTHENTICATION SERVICE nel parametro della matrice asAuthSvc passato a [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) Il client può specificare Snego chiamando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) e passando RPC \_ C \_ AUTHN \_ GSS NEGOTIATE come parametro \_ *dwAuthnSvc.* Il client deve anche fornire un elenco di possibili servizi di autenticazione per Snego tramite il membro **PackageList** della struttura [**SEC \_ WINNT \_ AUTH \_ IDENTITY \_ EX**](/windows/desktop/api/sspi/ns-sspi-_sec_winnt_auth_identity_exa) che viene passato al *parametro pAuthInfo* nella chiamata a **CoSetProxyBlanket**. Se *pAuthInfo* è **NULL,** Snego compone un elenco di servizi di autenticazione dai pacchetti di sicurezza installati nel computer. Snego invia quindi l'elenco dei servizi di autenticazione al server, confronta l'elenco con i servizi di autenticazione disponibili del server e seleziona un servizio di autenticazione da usare per la connessione.

> [!Note]  
> Schannel non può essere in elenco dei servizi di autenticazione utilizzati da Snego.

 

I client possono anche specificare Snego quando chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). I *parametri dwAuthnSvc* e *pAuthInfo* di [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) diventano membri di una struttura [**SOLE AUTHENTICATION \_ \_ INFO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) passata a **CoInitializeSecurity** tramite il *relativo parametro pAuthList.* I dettagli dei valori di tali membri sono gli stessi descritti nel paragrafo precedente.

Se si usa Snego, le chiamate a [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket) o [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) restituiranno Snego come servizio di autenticazione, anziché il servizio di autenticazione effettivo scelto da Snego per stabilire la connessione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Com e pacchetti di sicurezza](com-and-security-packages.md)
</dt> </dl>

 

 