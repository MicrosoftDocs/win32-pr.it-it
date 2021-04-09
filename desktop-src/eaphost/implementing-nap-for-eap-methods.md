---
title: Implementazione del supporto NAP per i metodi EAP
description: Informazioni su come implementare il supporto di protezione accesso alla rete per un supplicant EAPHost. Vedere gli argomenti relativi a protezione accesso alla rete correlati a EAPHost e visualizzare altre risorse disponibili.
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5f0bc8900ee3d9cb01edb79b64b8ef5a68df4c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "104047633"
---
# <a name="implementing-nap-support-for-eap-methods"></a>Implementazione del supporto NAP per i metodi EAP

In questo argomento viene illustrato come implementare NAP per un supplicant EAPHost. In Windows Vista e Windows Server 2008 è disponibile un client di imposizione di protezione accesso alla rete (NAP EC) per le connessioni autenticate [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .

## <a name="implementing-network-access-protection-nap"></a>Implementazione di protezione accesso alla rete (NAP)

Per supportare NAP, un supplicant EAPHost implementa una funzione di callback che corrisponde al prototipo di callback [**NotificationHandler**](/previous-versions/windows/desktop/api) e deve fornire un puntatore a questa funzione di callback durante la chiamata di [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).

La funzione di callback accetta due parametri.

-   GUID che identifica in modo univoco l'interfaccia associata all'autenticazione.
-   Puntatore VOID a una struttura di dati opaca fornita dal supplicar.

EAPHost chiamerà la funzione di callback fornita dal richiedente con il GUID dell'interfaccia univoco e il puntatore VOID quando lo stato di quarantena del computer viene modificato. Quando EAPHost chiama la funzione di callback fornita dal richiedente, il supplicant risponde chiudendo la connessione di rete logica identificata dal puntatore GUID/VOID dell'interfaccia e inizia di nuovo l'autenticazione con **EapHostPeerBeginSession**.

EAPHost può chiamare la funzione di callback fornita da supplicant in qualsiasi momento: prima, durante un'autenticazione attiva o dopo il completamento dell'autenticazione (dopo la chiamata di [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) ma non prima della chiamata a [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) ). Il richiedente risponde sempre chiudendo la connessione di rete logica ed eseguendo di nuovo l'autenticazione.

Se il richiedente si sta arrestando o scegliendo di non ricevere più notifiche relative alle modifiche dello stato di isolamento, il supplicant deve chiamare [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) e specificare il GUID dell'interfaccia appropriato. Se il richiedente desidera determinare l'isolamento della connessione di rete logica, il supplicant può ottenere tali informazioni da **EapHostPeerMethodResult. isolationState** quando [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) viene ottenuto da [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).

## <a name="eaphost-related-nap-information"></a>Informazioni su protezione accesso alla rete correlate a EAPHost

Per informazioni su NAP correlate all'API EAPHost, vedere gli argomenti seguenti.

-   [**\_tipo di attributo EAP \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [**\_errore EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [Domande frequenti sul richiedente EAPHost](eaphost-supplicant-frequently-asked-questions.md)
-   [**Proprietà del metodo EAP**](eap-method-properties.md)
-   [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [**Costanti di errore e informazioni correlate a EAP**](eap-related-error-and-information-constants.md)
-   [**stato di isolamento \_**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [**NotificationHandler**](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a>Risorse aggiuntive


-   Per un elenco delle risorse NAP, vedere [Protezione accesso alla rete](https://go.microsoft.com/fwlink/p/?linkid=84107).
-   Per informazioni sullo stato di integrità, vedere la pagina relativa [al rapporto di integrità (NAP, Network Access Protection) dei messaggi di](https://go.microsoft.com/fwlink/p/?linkid=83918)integrità.
-   Per la pagina Web del gruppo di rete aziendale e il Blog, vedere [Protezione accesso alla rete (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).
-   Per informazioni sull'API NAP, vedere [Protezione accesso alla rete](/windows/desktop/NAP/network-access-protection-start-page).


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione dell'interfaccia utente del metodo EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Abilitazione di Criteri di gruppo](enabling-group-policy.md)
</dt> <dt>

[Implementazione del supporto di In-Band NAP per i metodi EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Trasferimento di dati tra i metodi supplicant e EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Supplicant EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 