---
title: Implementazione del meccanismo LEAP di EAPHost
description: Viene descritto il meccanismo EAPHost che consente a terze parti di scrivere moduli LEAP (Lightweight Extensible Authentication Protocol) per Windows.
ms.assetid: d17a99cb-4a43-4719-984e-b742c9518f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc50cda8d32cc26dd81af5733345deebb579c792
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104118618"
---
# <a name="implementing-the-eaphost-leap-mechanism"></a>Implementazione del meccanismo LEAP di EAPHost

In questo argomento viene descritto il meccanismo EAPHost che consente a terze parti di scrivere moduli LEAP (Lightweight Extensible Authentication Protocol) per Windows. LEAP è un metodo di autenticazione legacy, creato da Cisco, in base allo [standard RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016). Per ulteriori informazioni su LEAP, vedere [la pagina relativa a Cisco LEAP Q&A](https://go.microsoft.com/fwlink/p/?linkid=84018).

## <a name="eaphost-authentication-process"></a>Processo di autenticazione EAPHost

Il normale processo di autenticazione EAPHost si verifica nel modo seguente:

-   L'autenticatore invia una richiesta di autenticazione del peer. Ad esempio, l'applicazione chiama [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) con la configurazione EAPHost e i dati utente.
-   Il peer invia un pacchetto di risposta in risposta a una richiesta valida. Ad esempio, una chiamata riuscita restituisce un handle di sessione dell' **\_ \_ handle di sessione EAP** .
-   L'autenticatore Invia un pacchetto di richiesta aggiuntivo e il peer risponde con una risposta. Ad esempio, l'applicazione chiama [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket) per ottenere i pacchetti EAP ricevuti da EAPHost durante la sessione. Ogni pacchetto viene elaborato da una chiamata a [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket).
-   [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket) restituirà sempre un codice di azione. Il supplicant deve quindi chiamare la funzione corrispondente al codice dell'azione.
-   La sequenza di richieste e risposte continua fino a quando necessario. Ad esempio, l'applicazione può chiamare [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) per richiedere gli attributi EAP disponibili e il peer risponde con [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) per restituirli.
-   Dopo una richiesta iniziale, non è possibile inviare una nuova richiesta fino a quando non viene ricevuta una risposta valida.
-   La conversazione continua fino a quando l'autenticatore non è in grado di autenticare il peer, nel qual caso l'implementazione dell'autenticatore deve trasmettere un errore EAP. Ad esempio, le risposte non accettabili a una o più richieste potrebbero causare la trasmissione di un errore EAP del codice 4.
-   In alternativa, la conversazione di autenticazione può continuare fino a quando l'autenticatore non determina l'esito positivo dell'autenticazione, nel qual caso l'autenticatore deve trasmettere un esito positivo EAP (codice 3).
-   Se il risultato indica esito positivo o negativo, l'applicazione chiama [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) per terminare la sessione. In caso di errore, è possibile tentare di ripetere l'autenticazione aprendo un'altra sessione con EAPHost e fornendo la stessa o una nuova identità.

### <a name="leap-authentication-process"></a>Processo di autenticazione LEAP

Il processo di autenticazione LEAP differisce dal normale processo di autenticazione EAPhost, come indicato di seguito:

-   L'autenticazione EAP viene avviata dal server (Authenticator). LEAP, al contrario, viene avviato dal client (peer).
    -   Pertanto, quando si scrive un modulo LEAP è sempre necessario assicurarsi che il pacchetto di richiesta di verifica dal metodo peer e la risposta EAP dal server EAP dispongano sempre dello stesso ID pacchetto del pacchetto EAP Success dal server.

    <!-- -->

    -   Al contrario, la richiesta e la risposta EAPHost e i pacchetti di successo hanno in genere tutti ID diversi.
        > [!Note]  
        > Ogni richiesta EAP dispone di un campo di tipo per indicare gli elementi richiesti. Come per il pacchetto di richiesta, ogni pacchetto di risposta EAP contiene un campo di tipo, che corrisponde al campo tipo della richiesta. Gli esempi includono i pacchetti di richiesta di identità e di richiesta di verifica.

         

-   In caso di errore con EAPHost, è possibile tentare di ripetere l'autenticazione aprendo un'altra sessione con EAPHost e fornendo la stessa identità o una nuova identità.

### <a name="leap-authenticator-method-implementation"></a>Implementazione del metodo LEAP Authenticator

Quando si sviluppa un metodo LEAP Authenticator, verificare quanto segue:

-   I metodi LEAP Authenticator devono restituire il codice dell'azione di [**\_ invio della \_ \_ risposta \_ dell'autenticatore del metodo EAP**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) dopo la prima fase di autenticazione (autenticazione peer). Quindi, quando viene chiamato [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) , deve restituire un [**EapPacket**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket) valido con il codice EAP [**EapCodeSuccess**](/windows/win32/api/eapmethodtypes/ne-eapmethodtypes-eapcode).
-   I metodi LEAP Authenticator devono restituire il codice dell'azione del [**\_ risultato della \_ \_ risposta \_ dell'autenticatore del metodo EAP**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) se la prima fase dell'autenticazione peer ha avuto esito negativo.
-   I metodi LEAP Authenticator devono restituire il pacchetto di risposta di autenticazione finale con il codice di azione del [**risultato della \_ \_ \_ risposta \_ dell'autenticatore del metodo EAP**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) quando viene chiamato [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) . Quindi, nelle chiamate successive a [**EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) è necessario restituire l' **\_ \_ handle di sessione EAP** per identificare la sessione autenticata.
-   

### <a name="leap-peer-method-implementation"></a>Implementazione del metodo peer intercalare

Quando si sviluppa un metodo di peer intercalare, verificare quanto segue:

-   I metodi del peer intercalare devono restituire il codice dell'azione [**EapPeerMethodResponseActionSend**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) dopo la prima fase di autenticazione (autenticazione peer) riuscita.
-   I metodi del peer intercalare devono restituire il codice dell'azione [**EapPeerMethodResponseActionResult**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) dopo che la seconda fase dell'autenticazione ha avuto esito positivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sequenza di chiamate EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Uso di EAPHost](using-eap-host.md)
</dt> </dl>

 

 




