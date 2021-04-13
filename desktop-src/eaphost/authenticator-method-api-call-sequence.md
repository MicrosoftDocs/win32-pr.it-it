---
title: Sequenza di chiamate API del metodo Authenticator
description: Informazioni sulla sequenza di chiamate API del metodo Authenticator. Vedere un elenco che illustra la sequenza di chiamate effettuate da un EAPHost su un metodo di autenticazione EAP.
ms.assetid: 4756300c-5e49-44e8-ab49-1993d780d2a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bb5c7d64bfe6e38ebb97550dc76fe8ffcae8176
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399727"
---
# <a name="authenticator-method-api-call-sequence"></a>Sequenza di chiamate API del metodo Authenticator

Questo argomento fornisce la sequenza di chiamate specifica per l'API del metodo Authenticator. Durante una tipica sessione di autenticazione EAP, EAPHost esegue una serie di chiamate su un metodo EAP che implementano le API del metodo di autenticazione EAPHost.

Nell'elenco seguente viene illustrata la sequenza di chiamate effettuate da EAPHost su un metodo di autenticazione EAP.

-   L'autenticatore EAP carica prima di tutto la DLL del metodo EAP utilizzata per l'autenticazione specifica in un server dei criteri di rete o in un altro server di autenticazione.
-   Chiama [**EapAuthenticatorGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) sul metodo con una struttura di [**\_ tipo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type) popolata per ottenere un elenco di puntatori alle funzioni implementate nella dll. Si presuppone che le chiamate di funzione successive da parte dei metodi di autenticazione (Server) vengano implementate nella DLL.
-   Chiama [**EapAuthenticatorInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) per indicare alla libreria di metodi EAP di preparare almeno una sessione di autenticazione utilizzando questo metodo di autenticazione.
-   Chiama [**EapMethodAuthenticatorBeginSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession) per stabilire una sessione di autenticazione univoca.
-   Ripete i passaggi seguenti fino a quando [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) non indica che è disponibile un risultato di autenticazione.
    -   Chiama [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) con un puntatore a un pacchetto di richiesta da passare al supplicante.
    -   Chiama [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) per recuperare il pacchetto di risposta inviato dal supplicant. Questa funzione restituisce un codice di **\_ azione di \_ \_ risposta \_ dell'autenticatore del metodo EAP** che indica l'azione successiva che l'autenticatore deve eseguire nella sessione di autenticazione EAP.
    -   Se il codice dell'azione è la [ \_ risposta di autenticazione del metodo \_ \_ \_ EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action), indica che il metodo EAP dispone di attributi disponibili affinché l'autenticatore recuperi e passi al metodo peer. L'autenticatore chiama [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) per ottenere i vari attributi di autenticazione EAP dal metodo di autenticazione EAP. Dopo che l'autenticatore ha elaborato gli attributi, chiama [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) che fornisce attributi di autenticazione EAP aggiornati per impostare il metodo di autenticazione EAP. Questa funzione restituisce un codice di **\_ azione di \_ \_ risposta \_ dell'autenticatore del metodo EAP** che determina l'azione successiva.
-   Se il codice dell'azione è il [ \_ risultato della \_ \_ risposta \_ dell'autenticatore del metodo EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action), significa che l'autenticatore ha determinato i risultati della sessione di autenticazione e che tali risultati sono disponibili per EAPHost. L'autenticatore chiama [**EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) e ottiene i risultati della sessione di autenticazione.
-   Questa operazione è seguita da una chiamata a [**EapMethodAuthenticatorEndSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession) per terminare la sessione di autenticazione.
-   Infine, viene eseguita una chiamata a [**EapMethodAuthenticatorShutdown**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown) per scaricare la dll del metodo di autenticazione.
-   Scarica la libreria di metodi EAP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_azione di \_ risposta dell'autenticatore del metodo EAP \_ \_**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)
</dt> <dt>

[Sequenza di chiamate API supplicant](supplicant-api-call-sequence.md)
</dt> <dt>

[Sequenza di chiamate API del metodo peer](peer-method-api-call-sequence.md)
</dt> <dt>

[Sequenze di chiamate EAPHost](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




