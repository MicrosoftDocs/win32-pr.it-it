---
title: Sequenza di chiamate API supplicant
description: Informazioni sulla sequenza di chiamate dell'API supplicant. Vedere una panoramica della sequenza di chiamate e visualizzare altre risorse disponibili.
ms.assetid: 83276783-aee5-43ac-982d-1144df982a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c93afea6dbf4c3220bbeaec4f6278eb3d0b756
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963473"
---
# <a name="supplicant-api-call-sequence"></a>Sequenza di chiamate API supplicant

Questo argomento fornisce la sequenza di chiamate specifica per l'API supplicant.

## <a name="supplicant-api-call-sequence-overview"></a>Panoramica della sequenza di chiamate dell'API supplicant

Quando il richiedente riceve un pacchetto EAP da un provider, ad esempio un punto di accesso, si verifica in genere il flusso di chiamate API di supplicar seguente.

-   L'applicazione chiama [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) con dati di configurazione EAPHost e dati utente. Una chiamata riuscita restituisce un handle di sessione dell' **\_ \_ handle di sessione EAP** .
-   Ogni pacchetto ricevuto dal supplicant viene elaborato da una chiamata a [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket). Il supplicant chiama quindi la funzione corrispondente al codice dell'azione restituito dalla funzione.
-   Se il codice dell'azione è **EapHostPeerResponseSend**, il supplicant chiama [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket) per ottenere la risposta da inviare all'autenticatore.
-   Se durante la sessione, il codice dell'azione restituito al richiedente è **EapHostPeerResponseRespond**, indica che gli attributi EAP sono disponibili. Il supplicant chiama quindi [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) per ottenerli. Questi attributi contengono dati supplementari usati durante il processo di autenticazione. Al termine dell'elaborazione degli attributi, il richiedente chiama [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) che aggiorna i dati. Questa funzione restituisce un codice di azione che determina l'azione successiva del richiedente.
-   Se il codice dell'azione è **EapHostPeerResponseInvokeUI** , il supplicant genera una finestra di dialogo dell'interfaccia utente per ottenere dati interattivi dall'utente, ad esempio le credenziali o le informazioni di identità. Vedere l'intervento dell'utente con il flusso di chiamate API supplicar di seguito.
-   Se il codice dell'azione è **EapHostPeerResponseResult**, indica che i risultati della sessione di autenticazione sono disponibili per il richiedente. Il supplicant chiama quindi [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult) per ottenere i risultati. Indipendentemente dal fatto che i risultati indichino l'esito positivo o negativo, il supplicant chiama [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession). In caso di errore, è possibile tentare di ripetere l'autenticazione aprendo un'altra sessione con EAPHost e fornendo una nuova identità oppure ritentando l'autenticazione con l'identità originale.

## <a name="user-interaction-with-the-supplicant-api-call-flow"></a>Interazione dell'utente con il flusso di chiamata dell'API supplicant

In alcuni casi, il richiedente deve ottenere informazioni dall'utente per continuare il processo di autenticazione.

Nell'elenco seguente viene illustrata la sequenza di chiamate sul processo dell'interfaccia utente supplicant e EAPHost necessario per abilitare l'input interattivo.

1.  Il supplicant ottiene il contesto dell'interfaccia utente corrente chiamando [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext).
2.  Il supplicant invia quindi i dati del contesto dell'interfaccia utente al processo dell'interfaccia utente del richiedente.
    > [!Note]  
    > Il processo dell'interfaccia utente, che in genere raccoglie l'interfaccia utente o gestisce l'interfaccia utente interattiva, è separato dal processo di supplicant. La separazione dei due processi non è un requisito di EAPHost, ma questa operazione ha il vantaggio di consentire al processo dell'interfaccia utente di interagire con il desktop.

     

3.  Se il supplicante desidera eseguire il rendering dell'interfaccia utente da solo, chiama la funzione [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) per ottenere i campi di input per i componenti dell'interfaccia utente interattivi da generare. In caso contrario, segue il modello tradizionale di richiamo dell'interfaccia utente interattiva del metodo chiamando [ **EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)
    > [!Note]  
    > Se viene restituito l' [**operazione del \_ metodo EAP E \_ EAPHOST \_ \_ \_ \_**](eap-related-error-and-information-constants.md) , il richiedente deve seguire il modello tradizionale di richiamo dell'interfaccia utente interattiva del metodo chiamando [**EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui). Se si verifica un errore, [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) restituirà un codice restituito diverso da **null**.

     

4.  Indica se il richiedente chiama [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) o [**EaphostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) il processo dell'interfaccia utente passa i dati di contesto esistenti e carica Eappcfg.dll. Viene generata un'interfaccia utente appropriata per raccogliere i nuovi dati. I nuovi dati del contesto dell'interfaccia utente, che possono ora contenere l'input dell'utente, vengono copiati e i dati di contesto obsoleti vengono rilasciati con una chiamata a [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory).
5.  Il processo dell'interfaccia utente restituisce i nuovi dati di contesto al supplicant, che chiama [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) per impostarlo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sequenza di chiamate API del metodo peer](peer-method-api-call-sequence.md)
</dt> <dt>

[Sequenza di chiamate API del metodo Authenticator](authenticator-method-api-call-sequence.md)
</dt> <dt>

[Sequenza di chiamate EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Supplicant EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




