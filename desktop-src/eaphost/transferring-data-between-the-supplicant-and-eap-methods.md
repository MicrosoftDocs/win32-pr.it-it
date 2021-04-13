---
title: Trasferimento di dati tra i metodi supplicant e EAP
description: Informazioni sul trasferimento di dati tra i metodi supplicant e EAP. Il trasferimento dei dati tra i metodi viene eseguito tramite gli attributi EAP.
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187858347e8630bfbaba0683700eaa39f116f6ce
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399734"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a>Trasferimento di dati tra i metodi supplicant e EAP

L'uso di attributi EAP consente lo scambio di dati tra supplicant e metodi EAP.

## <a name="attribute-consumption"></a>Utilizzo degli attributi

[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) utilizza gli attributi EAP passati direttamente al metodo EAP configurato. Analogamente, i metodi EAP possono restituire un codice di azione che indica al supplicant che gli attributi sono disponibili e che devono raccogliere gli attributi utilizzando [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).

Per ulteriori informazioni, vedere gli argomenti seguenti.

-   Codici di azione del richiedente [peer EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).
-   [Codici motivo della supplicant peer EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).
-   [Codici di azione del metodo di autenticazione EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).

Si prevede che i supplicant ignorino gli attributi che non riconoscono o non possono agire. Utilizzando [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) questi attributi ignorati vengono restituiti a EAPHost e al metodo EAP.

## <a name="vendor-specific-attributes"></a>Attributi specifici del fornitore

Utilizzando l'attributo EAP specifico del fornitore, i metodi e i supplicant EAP possono coinvolgere lo scambio di dati per uno scopo specifico. Gli attributi specifici del fornitore vengono ignorati dai supplicant e dai metodi che non supportano l'attributo specifico del fornitore.

Per ulteriori informazioni, vedere gli argomenti seguenti.

-   [Attributi EAP](about-eap-attributes.md).
-   [**EAP \_ \_tipo di attributo**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione dell'interfaccia utente del metodo EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Abilitazione di Criteri di gruppo](enabling-group-policy.md)
</dt> <dt>

[Implementazione del supporto di In-Band NAP per i metodi EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementazione del supporto NAP per i metodi EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Supplicant EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




