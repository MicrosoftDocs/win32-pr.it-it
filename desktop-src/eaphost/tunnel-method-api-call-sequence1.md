---
title: Sequenza di chiamate API del metodo tunnel
description: Informazioni sulla sequenza di chiamate API per i metodi di tunneling. Vedere una panoramica e visualizzare altre risorse disponibili.
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5f6b30fda111162585fb5c8b2aa370fa6af61e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339302"
---
# <a name="tunnel-method-api-call-sequence"></a>Sequenza di chiamate API del metodo tunnel

In questo argomento viene illustrata la sequenza di chiamate API per i metodi tunnel

## <a name="tunnel-method-call-sequence-overview"></a>Panoramica della sequenza di chiamate al metodo tunnel

Quando richiedente viene richiesta l'identità dell'utente e i dati utente, viene in genere generato il flusso di chiamate API seguente.

-   Il supplicant chiama EapHostPeerProcessReceivedPacket su EapHost per elaborare il pacchetto ricevuto dall'autenticatore.
-   Quando si elabora questo pacchetto, EAPHost lo determina come pacchetto IdentityRequest e chiama [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) sul metodo tunnel per ottenere l'identità utente da usare per l'autenticazione.
-   Se il metodo tunnel deve ottenere l'identità dell'utente dal metodo interno, chiama [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) su EAPHost interno, che a sua volta chiama [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) sul metodo interno.

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a>Interazione dell'utente con il flusso di chiamate API dei metodi tunnel

In alcuni casi, quando l'identità non è disponibile o quando l'utente deve fornire informazioni aggiuntive, il metodo EAP genera una finestra di dialogo dell'interfaccia utente nel supplicant.

In questi casi, la sequenza di chiamate viene in genere svolta per ottenere informazioni direttamente dall'utente.

-   Il metodo EAP del tunnel restituisce il codice dell'azione per richiamare l'interfaccia utente in EapHost. Supplicant chiama [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)per ottenere le informazioni sul contesto dell'interfaccia utente corrente per la finestra di dialogo dell'interfaccia utente.
-   Supplicant chiama quindi [ **EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) Questa funzione utilizza le informazioni sul contesto dell'interfaccia utente per generare un'interfaccia utente interattiva utilizzata per ottenere informazioni sulle credenziali dall'utente. Il processo dell'interfaccia utente carica Eappcfg.dll e ottiene i puntatori a EapPeerInvokeInteractiveUI e EapPeerFreeMemory.
    > [!Note]  
    > Il processo dell'interfaccia utente in genere raccoglie l'interfaccia utente o gestisce l'interfaccia utente interattiva ed è separato dal processo di supplicant. La separazione dei due processi non è un requisito di EAPHost, ma questa operazione ha il vantaggio di consentire al processo dell'interfaccia utente di interagire con il desktop.

     

-   EapHost chiama [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) sul metodo tunnel per ottenere informazioni sull'identità dell'utente.
-   Per ottenere l'identità dell'utente dal metodo interno, il metodo tunnel chiama [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) sull'EAPHost interno.
-   EAPHost interno chiama [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) sul metodo interno per richiamare l'interfaccia utente dell'identità utente.
-   [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) fornisce informazioni sul contesto dell'interfaccia utente nuove o aggiornate al metodo peer EAP caricato in EAPHost dopo la generazione dell'interfaccia utente.

Il diagramma seguente illustra la sequenza di chiamate API per i metodi tunnel

![sequenza di chiamate API di metodi tunnel](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sequenza di chiamate EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Sequenza di chiamate API supplicant](supplicant-api-call-sequence.md)
</dt> <dt>

[Informazioni di riferimento sull'API del richiedente EAPHost](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




