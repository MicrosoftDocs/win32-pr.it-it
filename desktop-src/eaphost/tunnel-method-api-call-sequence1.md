---
title: Tunnel Sequenza di chiamate api dei metodi
description: Informazioni sulla sequenza di chiamate API per Tunnel metodi. Vedere una panoramica e visualizzare altre risorse disponibili.
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca32a889229b6cdbdb3f008ebea8b838f9b6d64fba36bc2a30c4ddd9d62ac83d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272794"
---
# <a name="tunnel-method-api-call-sequence"></a>Tunnel Sequenza di chiamate api dei metodi

Questo argomento illustra la sequenza di chiamate API per Tunnel metodi

## <a name="tunnel-method-call-sequence-overview"></a>Tunnel Cenni preliminari sulla sequenza di chiamate al metodo

Quando Supplicant ottiene la richiesta di identità utente e dati utente, si verifica in genere il flusso di chiamate API seguente.

-   Il supplicant chiama EapHostPeerProcessReceivedPacket in EapHost per elaborare il pacchetto ricevuto dall'autenticatore.
-   Al momento dell'elaborazione di questo pacchetto, EAPHost lo determina come pacchetto IdentityRequest e chiama [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) sul metodo tunnel per ottenere l'identità utente da usare per l'autenticazione.
-   Se il metodo tunnel deve ottenere l'identità utente dal metodo interno, chiama [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) su EAPHost interno, che a sua volta chiama [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) sul metodo interno.

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a>Interazione dell'utente con Tunnel metodi di gestione delle Flow

In alcuni casi, quando l'identità non è disponibile o quando l'utente deve fornire informazioni aggiuntive, il metodo Eap genera una finestra di dialogo dell'interfaccia utente sul supplicant.

In questi casi si verifica in genere la sequenza di chiamate per ottenere informazioni direttamente dall'utente.

-   Tunnel Il metodo Eap restituisce il codice azione per richiamare l'interfaccia utente a EapHost. Supplicant chiama [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)per ottenere le informazioni sul contesto dell'interfaccia utente corrente per la finestra di dialogo dell'interfaccia utente.
-   Supplicant chiama quindi [ **EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) Questa funzione usa le informazioni sul contesto dell'interfaccia utente per generare un'interfaccia utente interattiva usata per ottenere informazioni sulle credenziali dall'utente. Il processo dell'interfaccia Eappcfg.dll e ottiene i puntatori a EapPeerInvokeInteractiveUI ed EapPeerFreeMemory.
    > [!Note]  
    > Il processo dell'interfaccia utente raccoglie in genere l'interfaccia utente o gestisce l'interfaccia utente interattiva ed è separato dal processo supplicant. La separazione dei due processi non è un requisito di EAPHost, ma ha il vantaggio di consentire al processo dell'interfaccia utente di interagire con il desktop.

     

-   EapHost chiama [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) sul metodo tunnel per ottenere informazioni sull'identità dell'utente.
-   Per ottenere l'identità utente dal metodo interno, il metodo tunnel chiama [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) su EAPHost interno.
-   Inner EAPHost chiama [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) sul metodo interno per richiamare l'interfaccia utente dell'identità utente.
-   [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) fornisce informazioni sul contesto dell'interfaccia utente nuove o aggiornate al metodo peer EAP caricato in EAPHost dopo la creazione dell'interfaccia utente.

Il diagramma seguente illustra la sequenza di chiamate API per Tunnel metodi

![sequenza di chiamate api dei metodi tunnel](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sequenza di chiamate EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Sequenza di chiamate API supplicant](supplicant-api-call-sequence.md)
</dt> <dt>

[Informazioni di riferimento sulle API supplicant EAPHost](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




