---
title: Implementazione del supporto di In-Band NAP per i metodi EAP
description: Può essere abilitato per i metodi EAP EAPHost che supportano la trasmissione di oggetti di tipo Length-Value (TLVs).
ms.assetid: 298c89d9-7a6a-4280-9af9-77c7c00cab92
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9eae9fc17e99b27f620fbab1ed42cbd4b73800
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734615"
---
# <a name="implementing-in-band-nap-support-for-eap-methods"></a>Implementazione del supporto di In-Band NAP per i metodi EAP

È possibile abilitare il supporto di [Protezione accesso alla rete](/windows/desktop/NAP/network-access-protection-start-page) (NAP) in banda per un metodo EAP per i metodi EAP EAPHost che supportano la trasmissione di oggetti con valori di tipo Length (TLVs). Quando è abilitato il supporto di protezione accesso alla rete in banda, i pacchetti NAP vengono trasportati all'interno di pacchetti di metodi EAP.

Al contrario, quando è abilitato il supporto di protezione accesso alla rete fuori banda, lo scambio del [rapporto di integrità di](https://go.microsoft.com/fwlink/p/?linkid=83917) protezione accesso alla rete (SOH) viene eseguito tramite mezzi diversi dai pacchetti di metodi EAP.

Tutti TLVs sono specifici del fornitore.

## <a name="implementing-nap-support-on-eap-peer-methods"></a>Implementazione del supporto NAP nei metodi peer EAP

L'implementazione del metodo peer EAP riceve un TLV che contiene il valore TLV della richiesta del [rapporto di integrità](https://go.microsoft.com/fwlink/p/?linkid=83917) da un server EAP.

L'implementazione del metodo peer EAP passa quindi la TLV che contiene la richiesta di rapporto di integrità TLV a EAPHost come indicato di seguito.

-   L'implementazione del metodo peer EAP restituisce il codice di azione [**EapPeerMethodResponseActionRespond**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) a EAPHost al ritorno da [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).
-   EAPHost chiama [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) dall'implementazione del metodo peer EAP. Gli attributi vengono passati nel processo.
-   L'implementazione del metodo peer EAP restituisce il TLV contenente la richiesta di rapporto di integrità in [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes). Gli attributi vengono ricevuti nel processo.

L'implementazione del metodo peer EAP riceve un TLV contenente un rapporto di integrità TLV da EAPHost, come indicato di seguito.

-   EAPHost chiama [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) dall'implementazione del metodo peer EAP. **EapPeerSetResponseAttributes** contiene un TLV che ospita un rapporto di integrità TLV.
-   L'implementazione del metodo peer EAP invia il rapporto di integrità TLV al server EAP.
-   L'implementazione del metodo peer EAP riceve un TLV contenente un TLV di risposta a rapporto di integrità dal server EAP.

L'implementazione del metodo peer EAP passa il TLV contenente la risposta di rapporto di integrità TLV a EAPHost, come indicato di seguito.

-   L'implementazione del metodo peer EAP restituisce il codice di azione **EapPeerMethodResponseActionRespond** a EAPHost al ritorno da [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).
-   EAPHost chiama [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) dalle implementazioni del metodo peer EAP. La struttura degli [**\_ attributi EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) viene passata nel processo.
-   L'implementazione del metodo peer EAP restituisce il TLV contenente la risposta di rapporto di integrità TLV in [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes).

> [!Note]  
> Il membro **eapType** della struttura [**dell' \_ attributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) sarà sempre impostato su **eatEAPTLV** e il membro **pValue** punterà al primo byte del TLV che contiene la risposta del rapporto di integrità TLV.

 

### <a name="implementing-nap-support-on-eap-server-methods"></a>Implementazione del supporto NAP nei metodi del server EAP

L'implementazione del metodo del server EAP costruisce un TLV contenente un TLV della richiesta di rapporto di integrità. L'implementazione del metodo del server EAP Invia questo TLV contenente la richiesta di rapporto di integrità TLV al peer EAP. L'implementazione del metodo del server EAP riceve la TLV dal peer EAP.

L'implementazione del metodo del server EAP passa il TLV contenente un rapporto di integrità TLV a EAPHost come indicato di seguito.

-   Tramite l'implementazione del metodo del server EAP viene restituita la **\_ risposta dell'autenticatore del metodo EAP del codice di azione che \_ \_ \_ risponde** a EAPHost al ritorno da [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket).
-   EAPHost chiama [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) dall'implementazione del metodo del server EAP.
-   L'implementazione del metodo del server EAP restituisce il TLV che contiene il rapporto di integrità TLV in [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes).

L'implementazione del metodo del server EAP riceve un TLV contenente una risposta di rapporto di integrità TLV da EAPHost, come indicato di seguito.

-   EAPHost chiama [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) dall'implementazione del metodo del server EAP.
-   Il TLV che contiene il rapporto di integrità della risposta TLV viene restituito in [ **EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)
-   L'implementazione del metodo del server EAP invia il TLV contenente la risposta di rapporto di integrità TLV.

> [!Note]  
> Il membro **eapType** della struttura [**dell' \_ attributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) sarà sempre impostato su **eatEAPTLV** e il membro **pValue** punterà al primo byte del TLV che contiene la risposta del rapporto di integrità TLV.

 

### <a name="messages"></a>Messaggi

Il protocollo EAP SoH TLV viene usato per incapsulare il protocollo di rapporto di integrità per la trasmissione tramite un metodo EAP. Tutti i TLVs EAP SoH hanno la stessa struttura, che differisce solo per l'ID del messaggio e la parte di dati del messaggio.

Per ulteriori informazioni, vedere [la pagina relativa ai messaggi del rapporto di integrità (NAP) di protezione accesso alla rete](https://go.microsoft.com/fwlink/p/?linkid=83918).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione dell'interfaccia utente del metodo EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Abilitazione di Criteri di gruppo](enabling-group-policy.md)
</dt> <dt>

[Implementazione del supporto NAP per i metodi EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Trasferimento di dati tra i metodi supplicant e EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Supplicant EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 