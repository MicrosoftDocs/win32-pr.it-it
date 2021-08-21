---
title: Configurazione del metodo EAP Interfaccia utente
description: Spiega come configurare il supplicante fornendo una configurazione del metodo EAP a EAPHost.
ms.assetid: f6a23201-e221-4098-863f-71a81735d927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6709e68bf20d8f38d3685f66e45313083e70e46b1a8a0bb0675616bdb4e8bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086705"
---
# <a name="configuring-the-eap-method-user-interface"></a>Configurazione del metodo EAP Interfaccia utente

Questo argomento illustra come configurare il supplicante fornendo una configurazione del metodo EAP a EAPHost.

Per poter eseguire un'autenticazione basata su EAP usando EAPHost, un supplicante deve fornire una configurazione del metodo EAP a EAPHost tramite la funzione [**EapHostPeerBeginSession.**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)

1.  Per ottenere la configurazione del metodo EAP, un supplicante in genere esegue una query EAPHost [**usando EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) per ottenere il set completo di metodi EAP disponibili e installati nel computer locale. L'elenco dei metodi viene in genere presentato all'utente in una casella combinata o in un altro controllo dell'interfaccia utente che consente all'utente di selezionare il metodo desiderato.
    > [!Note]  
    > Il supplicante può scegliere di filtrare l'elenco visualizzato di metodi in base ai bit delle proprietà dei metodi indicati in **EAP \_ METHOD \_ INFO.eapProperties**. Alcuni metodi potrebbero non essere appropriati per le caratteristiche di sicurezza del trasporto fornito dal supplicante, ad esempio.

     

2.  Dopo che il controllo dell'interfaccia utente è stato popolato con il set di possibili metodi EAP, l'utente seleziona il metodo che vuole configurare. In genere, il supplicante fornisce un **pulsante Configurazione** o **Proprietà** che consente all'utente di accedere alle proprietà di configurazione del metodo EAP selezionato.
    > [!Note]
    > Il supplicante è consapevole che esistono proprietà configurabili dall'utente basate sul bit **eapPropSupportsConfig** abilitato in **EAP \_ METHOD \_ INFO.eapProperties**.
    >
    > Per altre informazioni, vedere [**Proprietà del metodo EAP.**](eap-method-properties.md)

     

3.  Quando l'utente fa clic sul controllo dell'interfaccia utente appropriato, il supplicato chiama [**EapHostPeerInvokeConfigUI,**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui)passando nella funzione il valore **HWND** per l'interfaccia utente del supplicant, la struttura [**EAP \_ METHOD \_ TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) ottenuta dalla query alla struttura [**EAP \_ METHOD \_ INFO**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) e altri parametri obbligatori.
4.  La [**chiamata a EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) richiama l'interfaccia utente di configurazione di un metodo EAP. Al ritorno da **EapHostPeerInvokeConfigUI,** la funzione restituirà un BLOB di configurazione del metodo EAP come parametro out.
5.  Il supplicant archivia il BLOB di configurazione, insieme alla struttura [**EAP \_ METHOD \_ TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) da usare [**con EapHostPeerBeginSession.**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
6.  Il metodo preciso per archiviare il BLOB di configurazione dipende interamente dal supplicante. Tuttavia, il supplicante deve sempre archiviare la configurazione in modo appropriato e sicuro appropriato per i dati di configurazione di autenticazione utente e di sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Abilitazione Criteri di gruppo](enabling-group-policy.md)
</dt> <dt>

[Implementazione del In-Band protezione accesso alla rete per i metodi EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementazione del supporto di Protezione accesso alla rete per i metodi EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Trasferimento di dati tra i metodi supplicant ed EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Supplicant EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




