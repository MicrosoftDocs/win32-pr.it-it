---
title: Implementazione del In-Band protezione accesso alla rete per i metodi EAP
description: Può essere abilitato per i metodi EAPHost che supportano la trasmissione di oggetti TV (Type-Length-Value Objects).
ms.assetid: 298c89d9-7a6a-4280-9af9-77c7c00cab92
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477ad8f2ee033b3f98f9cac0e7ee34d18dc62f00dd5bd7c0e09509ad32bcfa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904277"
---
# <a name="implementing-in-band-nap-support-for-eap-methods"></a>Implementazione del In-Band protezione accesso alla rete per i metodi EAP

Il supporto di Protezione accesso alla rete (NAP, [Network Access Protection)](/windows/desktop/NAP/network-access-protection-start-page) in banda per un metodo EAP può essere abilitato per i metodi EAPHost che supportano la trasmissione di oggetti TV (Type-Length-Value Objects). Quando è abilitato il supporto di Protezione accesso alla rete in banda, i pacchetti di Protezione accesso alla rete vengono trasportati all'interno di pacchetti del metodo EAP.

Al contrario, quando è abilitato il supporto di Protezione accesso alla rete fuori banda, lo scambio di soh (Nap [Statement of Health)](https://go.microsoft.com/fwlink/p/?linkid=83917) avviene tramite mezzi diversi da quelli interni ai pacchetti del metodo EAP.

Tutte le TV sono specifiche del fornitore.

## <a name="implementing-nap-support-on-eap-peer-methods"></a>Implementazione del supporto di Protezione accesso alla rete nei metodi peer EAP

L'implementazione del metodo peer EAP riceve una TLV contenente la TLV della richiesta Statement [of Health](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) da un server EAP.

L'implementazione del metodo peer EAP passa quindi la TLV contenente la TLV della richiesta SoH a EAPHost come indicato di seguito.

-   L'implementazione del metodo peer EAP restituisce il codice di azione [**EapPeerMethodResponseActionRespond a**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) EAPHost al ritorno da [**EapPeerProcessRequestPacket.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)
-   EAPHost chiama [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) dall'implementazione del metodo peer EAP. Gli attributi vengono passati nel processo.
-   L'implementazione del metodo peer EAP restituisce il TLV contenente la TLV della richiesta SoH in [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes). Gli attributi vengono ricevuti nel processo.

L'implementazione del metodo peer EAP riceve un TLV contenente una TLV SoH da EAPHost come indicato di seguito.

-   EAPHost chiama [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) dall'implementazione del metodo peer EAP. **EapPeerSetResponseAttributes** contiene una TLV che ospita un TLV SoH.
-   L'implementazione del metodo peer EAP invia la TLV SoH al server EAP.
-   L'implementazione del metodo peer EAP riceve una TLV contenente una TLV di risposta SoH dal server EAP.

L'implementazione del metodo peer EAP passa la TLV contenente la TLV di risposta SoH a EAPHost come indicato di seguito.

-   L'implementazione del metodo peer EAP restituisce il codice azione **EapPeerMethodResponseActionRespond a** EAPHost al ritorno da [**EapPeerProcessRequestPacket.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)
-   EAPHost chiama [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) dalle implementazioni del metodo peer EAP. La [**struttura \_ ATTRIBUTES EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) viene passata nel processo.
-   L'implementazione del metodo peer EAP restituisce la TLV contenente la TLV di risposta SoH in [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes).

> [!Note]  
> Il membro **eapType** della struttura [**\_ ATTRIBUTE EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) sarà sempre impostato su **eatEAPTLV** e il membro **pValue** farà riferimento al primo byte della TLV che contiene il TLV di risposta SoH.

 

### <a name="implementing-nap-support-on-eap-server-methods"></a>Implementazione del supporto di Protezione accesso alla rete nei metodi del server EAP

L'implementazione del metodo server EAP costruisce una TLV contenente una TLV di richiesta SoH. L'implementazione del metodo server EAP invia questa TLV contenente la TLV della richiesta SoH al peer EAP. L'implementazione del metodo server EAP riceve la TLV dal peer EAP.

L'implementazione del metodo server EAP passa la TLV contenente un TLV SoH a EAPHost come indicato di seguito.

-   L'implementazione del metodo server EAP restituisce il codice di azione **EAP \_ METHOD \_ AUTHENTICATOR \_ RESPONSE \_ RESPOND** a EAPHost al ritorno da [**EapMethodAuthenticatorReceivePacket.**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket)
-   EAPHost chiama [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) dall'implementazione del metodo server EAP.
-   L'implementazione del metodo server EAP restituisce il TLV contenente la TLV SoH in [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes).

L'implementazione del metodo server EAP riceve una TLV contenente una TLV di risposta SoH da EAPHost come indicato di seguito.

-   EAPHost chiama [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) dall'implementazione del metodo server EAP.
-   La TLV contenente la TLV di risposta SoH viene restituita in [ **EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)
-   L'implementazione del metodo server EAP invia la TLV contenente la TLV di risposta SoH.

> [!Note]  
> Il membro **eapType** della struttura [**\_ ATTRIBUTE EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) sarà sempre impostato su **eatEAPTLV** e il membro **pValue** farà riferimento al primo byte della TLV che contiene il TLV di risposta SoH.

 

### <a name="messages"></a>Messaggi

Il TLV SoH EAP viene usato per incapsulare il protocollo SoH per la trasmissione tramite un metodo EAP. Tutte le TV soH EAP hanno la stessa struttura, differendo solo in base all'ID messaggio e alla parte di dati del messaggio.

Per altre informazioni, vedere [Messaggi soH (Network Access Protection) Statement of Health (NAP).](https://go.microsoft.com/fwlink/p/?linkid=83918)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione del metodo EAP Interfaccia utente](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Abilitazione Criteri di gruppo](enabling-group-policy.md)
</dt> <dt>

[Implementazione del supporto di Protezione accesso alla rete per i metodi EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Trasferimento di dati tra i metodi Supplicant ed EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Supplicant EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 