---
title: Authenticator Sequenza di chiamate API del metodo
description: Informazioni sulla sequenza di chiamate API del metodo di autenticazione. Vedere un elenco che illustra la sequenza di chiamate effettuate da un EAPHost su un metodo di autenticazione EAP.
ms.assetid: 4756300c-5e49-44e8-ab49-1993d780d2a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e3864d7b08c3c5c154ef3be86d0ac14716cd8b46adb1485fc5c55e598f870a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852291"
---
# <a name="authenticator-method-api-call-sequence"></a>Authenticator Sequenza di chiamate API del metodo

Questo argomento fornisce la sequenza di chiamata specifica per l'API del metodo di autenticazione. Durante una tipica sessione di autenticazione EAP, EAPHost effettua una serie di chiamate su un metodo EAP che implementano le API del metodo di autenticazione EAPHost.

L'elenco seguente illustra la sequenza di chiamate effettuate da EAPHost su un metodo di autenticazione EAP.

-   L'autenticatore EAP carica prima di tutto la DLL del metodo EAP usata per l'autenticazione specifica in un server dei criteri di rete o in un altro server di autenticazione.
-   Chiama [**EapAuthenticatorGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) sul metodo con una struttura [**TYPE EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type) popolata per ottenere un elenco di puntatori alle funzioni implementate nella DLL. Si presuppone che le chiamate di funzione successive da parte dei metodi di autenticazione (server) siano implementate nella DLL.
-   Chiama [**EapAuthenticatorInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) per indicare alla libreria del metodo EAP di preparare almeno una sessione di autenticazione usando questo metodo di autenticazione.
-   Chiama [**EapMethodAuthenticatorBeginSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession) per stabilire una sessione di autenticazione univoca.
-   Ripete i passaggi seguenti finché [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) non indica che è disponibile un risultato di autenticazione.
    -   Chiama [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) con un puntatore a un pacchetto di richiesta da passare al supplicante.
    -   Chiama [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) per recuperare il pacchetto di risposta inviato dal supplicant. Questa funzione restituisce un **codice EAP \_ METHOD \_ AUTHENTICATOR RESPONSE \_ \_ ACTION** che indica l'azione successiva che l'autenticatore deve eseguire nella sessione di autenticazione EAP.
    -   Se il codice di azione è [EAP \_ METHOD \_ AUTHENTICATOR \_ RESPONSE \_ RESPOND,](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)indica che il metodo EAP dispone di attributi disponibili per l'autenticatore da recuperare e passare al metodo peer. Authenticator chiama [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) per ottenere i vari attributi di autenticazione EAP dal metodo di autenticazione EAP. Dopo l'elaborazione degli attributi, l'autenticatore chiama [**EapMethodAuthenticatorSetAttributes,**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) che fornisce attributi di autenticazione EAP aggiornati da impostare nel metodo di autenticazione EAP. Questa funzione restituisce un **codice EAP \_ METHOD \_ AUTHENTICATOR RESPONSE \_ \_ ACTION** che determina l'azione successiva.
-   Se il codice azione è [EAP \_ METHOD \_ AUTHENTICATOR \_ RESPONSE \_ RESULT](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action), indica che l'autenticatore ha determinato i risultati della sessione di autenticazione e tali risultati sono disponibili per EAPHost. Authenticator chiama [**EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) e ottiene i risultati della sessione di autenticazione.
-   Questa operazione è seguita da una chiamata a [**EapMethodAuthenticatorEndSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession) per terminare la sessione di autenticazione.
-   Infine, viene effettuata una chiamata a [**EapMethodAuthenticatorShutdown**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown) per scaricare la DLL del metodo di autenticazione.
-   Scarica la libreria dei metodi EAP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**AZIONE DI RISPOSTA \_ \_ DELL'AUTENTICATORE \_ DEL METODO \_ EAP**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)
</dt> <dt>

[Sequenza di chiamate API supplicant](supplicant-api-call-sequence.md)
</dt> <dt>

[Sequenza di chiamate API del metodo peer](peer-method-api-call-sequence.md)
</dt> <dt>

[Sequenze di chiamata EAPHost](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




