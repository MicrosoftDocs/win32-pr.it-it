---
title: Sequenza di chiamate API del metodo peer
description: Informazioni sulla sequenza di chiamate API del metodo peer. Vedere un elenco che illustra la sequenza di chiamate effettuate da un EAPHost su un metodo peer EAP.
ms.assetid: aac69e89-249d-4bc8-baef-1f0681f9f7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac9be0f6de228fd5b1ebf2d2c28320baf76e914
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118463"
---
# <a name="peer-method-api-call-sequence"></a>Sequenza di chiamate API del metodo peer

Questo argomento fornisce la sequenza di chiamate specifica per l'API del metodo peer. Durante una tipica sessione di autenticazione EAP, EAPHost esegue una serie di chiamate sui metodi EAP per implementare l'API del metodo peer EAPHost.

Nell'elenco seguente viene illustrata la sequenza di chiamate effettuate da EAPHost su un metodo peer EAP.

-   Carica la DLL del metodo peer EAP utilizzata per l'autenticazione.
-   Chiama [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) sul metodo per ottenere un elenco di puntatori alle funzioni implementate nella dll. Si presuppone che le chiamate di funzione successive da parte del peer EAPHost (client) vengano implementate nella DLL.
-   Chiama [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) per indicare alla libreria di metodi EAP di preparare almeno una sessione di autenticazione utilizzando questo metodo peer.
-   Chiama [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) per stabilire una sessione di autenticazione univoca.
-   Chiama [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) per ottenere l'identità da usare per l'autenticazione. Se l'identità non è disponibile o se l'utente deve fornire informazioni aggiuntive, EAPHost chiama [ **EapPeerGetUIContext.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext) Questa funzione ottiene le informazioni sul contesto per la finestra di dialogo dell'interfaccia utente che verrà generata nel supplicar. Dopo che l'utente ha inviato le informazioni di identità, l'identità utente viene impostata con una chiamata a [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)e ottenuta da una chiamata a **EapPeerGetIdentity**.
-   Ripete i passaggi seguenti fino a quando [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) non indica che è disponibile un risultato di autenticazione.
    -   Chiama [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) con il puntatore di un pacchetto di richiesta da passare al supplicante.
    -   Chiama **EapPeerGetResponsePacket** per recuperare il pacchetto di risposta da inviare all'autenticatore.
    -   Facoltativamente, se è necessario recuperare o inviare attributi EAP durante la sessione di autenticazione, EAPHost chiama rispettivamente [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) e [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) .
-   Quando l'autenticatore Invia un codice di azione che indica che l'autenticazione è completa, EAPHost chiama [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult) e ottiene i risultati dell'autenticazione.
-   Chiama [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) per terminare la sessione di autenticazione.
-   Chiama [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown) per scaricare la dll del metodo peer.
-   Scarica la libreria di metodi EAP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sequenza di chiamate API supplicant](supplicant-api-call-sequence.md)
</dt> <dt>

[Sequenza di chiamate API del metodo Authenticator](authenticator-method-api-call-sequence.md)
</dt> <dt>

[Sequenze di chiamate EAPHost](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




