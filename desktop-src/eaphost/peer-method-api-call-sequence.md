---
title: Sequenza di chiamate API del metodo peer
description: Informazioni sulla sequenza di chiamate API del metodo peer. Vedere un elenco che illustra la sequenza di chiamate effettuate da un EAPHost su un metodo peer EAP.
ms.assetid: aac69e89-249d-4bc8-baef-1f0681f9f7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647a6a558d282ff4ae3691c23600b696b79764ee68a1007ccabb445c5a1fe65d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042789"
---
# <a name="peer-method-api-call-sequence"></a>Sequenza di chiamate API del metodo peer

Questo argomento fornisce la sequenza di chiamata specifica per l'API del metodo peer. Durante una tipica sessione di autenticazione EAP, EAPHost effettua una serie di chiamate ai metodi EAP per implementare l'API del metodo peer EAPHost.

L'elenco seguente illustra la sequenza di chiamate effettuate da EAPHost su un metodo peer EAP.

-   Carica la DLL del metodo peer EAP utilizzata per l'autenticazione.
-   Chiama [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) sul metodo per ottenere un elenco di puntatori alle funzioni implementate nella DLL. Si presuppone che le chiamate di funzione successive dal peer (client) EAPHost siano implementate nella DLL.
-   Chiama [**EapPeerInitialize per**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) indicare alla libreria di metodi EAP di preparare almeno una sessione di autenticazione usando questo metodo peer.
-   Chiama [**EapPeerBeginSession per**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) stabilire una sessione di autenticazione univoca.
-   Chiama [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) per ottenere l'identità da usare per l'autenticazione. Se l'identità non è disponibile o se l'utente deve fornire informazioni aggiuntive, EAPHost chiama [ **EapPeerGetUIContext.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext) Questa funzione ottiene le informazioni di contesto per la finestra di dialogo dell'interfaccia utente che verrà generata nel supplicante. Dopo che l'utente ha inviato le informazioni sull'identità, l'identità utente viene impostata con una chiamata a [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)e ottenuta da una chiamata a **EapPeerGetIdentity.**
-   Ripete i passaggi seguenti finché [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) non indica che è disponibile un risultato di autenticazione.
    -   Chiama [**EapPeerProcessRequestPacket con**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) il puntatore di un pacchetto di richiesta da passare al supplicant.
    -   Chiama **EapPeerGetResponsePacket per** recuperare il pacchetto di risposta da inviare all'autenticatore.
    -   Facoltativamente, se gli attributi EAP devono essere recuperati o inviati durante la sessione di autenticazione, EAPHost chiama [**rispettivamente EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) e [**EapPeerSetResponseAttributes.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)
-   Quando l'autenticatore invia un codice azione che indica che l'autenticazione è stata completata, EAPHost chiama [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult) e ottiene i risultati dell'autenticazione.
-   Chiama [**EapPeerEndSession per**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) terminare la sessione di autenticazione.
-   Chiama [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown) per scaricare la DLL del metodo peer.
-   Scarica la libreria di metodi EAP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sequenza di chiamate API supplicant](supplicant-api-call-sequence.md)
</dt> <dt>

[Authenticator Sequenza di chiamate API del metodo](authenticator-method-api-call-sequence.md)
</dt> <dt>

[Sequenze di chiamata EAPHost](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




