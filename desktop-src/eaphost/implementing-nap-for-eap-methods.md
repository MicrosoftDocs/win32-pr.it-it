---
title: Implementazione del supporto di Protezione accesso alla rete per i metodi EAP
description: Informazioni su come implementare il supporto di Protezione accesso alla rete per un supplicante EAPHost. Vedere gli argomenti relativi a Protezione accesso alla rete correlati a EAPHost e visualizzare altre risorse disponibili.
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00860057baeedbfdbae1939ab402db6f28fd74bd
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812382"
---
# <a name="implementing-nap-support-for-eap-methods"></a>Implementazione del supporto di Protezione accesso alla rete per i metodi EAP

In questo argomento viene illustrato come implementare Protezione accesso alla rete per una supplica EAPHost. In Windows Vista e Windows Server 2008 è disponibile un client di imposizione protezione accesso alla rete (NAP EC) per le connessioni autenticate [802.1X.](/previous-versions/windows/embedded/ms890287(v=msdn.10))

## <a name="implementing-network-access-protection-nap"></a>Implementazione di Protezione accesso alla rete

Per supportare Protezione accesso alla rete, un supplicante EAPHost implementa una funzione di callback corrispondente al prototipo di callback [**NotificationHandler**](/previous-versions/windows/desktop/api) e deve fornire un puntatore a questa funzione di callback quando si [**chiama EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).

La funzione di callback accetta due parametri.

-   GUID che identifica in modo univoco l'interfaccia associata all'autenticazione.
-   Puntatore VOID a una struttura di dati opaca fornita dal supplicant.

EAPHost chiamerà la funzione di callback fornita da supplicant con il GUID univoco dell'interfaccia e il puntatore VOID quando lo stato di quarantena del computer cambia. Quando EAPHost chiama la funzione di callback fornita da supplicant, il supplicante risponde tramite la rimozione della connessione di rete logica identificata dal puntatore VOID/GUID dell'interfaccia e avvia nuovamente l'autenticazione **usando EapHostPeerBeginSession.**

EAPHost può chiamare la funzione di callback fornita da supplicant in qualsiasi momento: prima, durante un'autenticazione attiva o dopo il completamento dell'autenticazione (dopo la chiamata di [**EapHostPeerEndSession,**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) ma non prima della chiamata di [**EapHostPeerClearConnection).**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) Il supplicante deve sempre rispondere tramite la rimozione della connessione di rete logica e la nuova autenticazione.

Se il supplicant si arresta o sceglie di non ricevere più la notifica delle modifiche dello stato di isolamento, il supplicante deve chiamare [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) e specificare il GUID dell'interfaccia appropriato. Se il supplicante vuole determinare l'isolamento della connessione di rete logica, il supplicante può ottenere queste informazioni da **EapHostPeerMethodResult.isolationState** quando [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) viene ottenuto da [**EapHostPeerGetResult.**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult)

## <a name="eaphost-related-nap-information"></a>Informazioni su Protezione accesso alla rete correlate a EAPHost

Per informazioni su Protezione accesso alla rete relative all'API EAPHost, vedere gli argomenti seguenti.

-   [**TIPO DI \_ ATTRIBUTO \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [**ERRORE \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [Domande frequenti su EAPHost Supplicant](eaphost-supplicant-frequently-asked-questions.yml)
-   [**Proprietà del metodo EAP**](eap-method-properties.md)
-   [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [**Costanti relative a errori e informazioni EAP**](eap-related-error-and-information-constants.md)
-   [**ISOLATION \_ STATE**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [**NotificationHandler**](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a>Risorse aggiuntive


-   Per un elenco delle risorse di Protezione accesso alla rete, vedere [Protezione accesso alla rete.](https://go.microsoft.com/fwlink/p/?linkid=84107)
-   Per informazioni sull'informativa sull'integrità, vedere [Network Access Protection (NAP) Statement of Health (SoH) Messages](https://go.microsoft.com/fwlink/p/?linkid=83918).
-   Per la pagina Enterprise e il blog del gruppo di rete, vedere Protezione accesso [alla rete](https://go.microsoft.com/fwlink/p/?linkid=83845).
-   Per informazioni sull'API protezione accesso alla rete, vedere [Protezione accesso alla rete.](/windows/desktop/NAP/network-access-protection-start-page)


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione del metodo EAP Interfaccia utente](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Abilitazione Criteri di gruppo](enabling-group-policy.md)
</dt> <dt>

[Implementazione del In-Band protezione accesso alla rete per i metodi EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Trasferimento di dati tra i metodi supplicant ed EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Supplicant EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 