---
title: Trasferimento di dati tra i metodi supplicant ed EAP
description: Informazioni sul trasferimento dei dati tra i metodi Supplicant ed EAP. Il trasferimento dei dati tra metodi viene ottenuto tramite attributi EAP.
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7675cac2c7e147804bc4c5ec86304e75063964bdc54cd44519fe535e28783f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085652"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a>Trasferimento di dati tra i metodi supplicant ed EAP

L'uso degli attributi EAP consente lo scambio di dati tra supplicant e metodi EAP.

## <a name="attribute-consumption"></a>Utilizzo attributi

[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) usa gli attributi EAP passati direttamente al metodo EAP configurato. Analogamente, i metodi EAP possono restituire un codice di azione che indica al supplicant che gli attributi sono disponibili e che devono raccogliere gli attributi [**usando EapHostPeerGetResponseAttributes.**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes)

Per ulteriori informazioni, vedere gli argomenti seguenti.

-   [Codici di azione supplicant peer EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).
-   [Codici motivo supplicant peer EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).
-   [Codici di azione Authenticator metodo EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).

Si prevede che i supplicant ignorino gli attributi che non riconoscono o su cui non possono agire. Usando [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) questi attributi ignorati vengono inviati nuovamente a EAPHost e al metodo EAP.

## <a name="vendor-specific-attributes"></a>Attributi specifici del fornitore

Usando l'attributo EAP specifico del fornitore, i metodi e i supplicant EAP possono impegnarsi nello scambio di dati per uno scopo specifico. Gli attributi specifici del fornitore vengono ignorati da supplicant e metodi che non supportano l'attributo specifico del fornitore.

Per ulteriori informazioni, vedere gli argomenti seguenti.

-   [Attributi EAP](about-eap-attributes.md).
-   [**EAP \_ TIPO \_ DI ATTRIBUTO**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione del metodo EAP Interfaccia utente](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Abilitazione Criteri di gruppo](enabling-group-policy.md)
</dt> <dt>

[Implementazione del In-Band protezione accesso alla rete per i metodi EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementazione del supporto di Protezione accesso alla rete per i metodi EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Supplicant EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




