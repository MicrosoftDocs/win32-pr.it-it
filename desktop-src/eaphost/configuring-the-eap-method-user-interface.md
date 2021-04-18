---
title: Configurazione dell'interfaccia utente del metodo EAP
description: Viene illustrato come configurare il supplicant fornendo una configurazione del metodo EAP a EAPHost.
ms.assetid: f6a23201-e221-4098-863f-71a81735d927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b82debadc075b1fcc12dad06484c0fd3617874
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299315"
---
# <a name="configuring-the-eap-method-user-interface"></a>Configurazione dell'interfaccia utente del metodo EAP

In questo argomento viene illustrato come configurare il supplicant fornendo una configurazione del metodo EAP a EAPHost.

Per chiedere a un richiedente di eseguire un'autenticazione basata su EAP mediante EAPHost, è necessario che un supplicant fornisca una configurazione del metodo EAP a EAPHost tramite la funzione [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) .

1.  Per ottenere la configurazione del metodo EAP, in genere un supplicant esegue una query su EAPHost usando [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) per apprendere il set completo di metodi EAP disponibili e installati nel computer locale. L'elenco dei metodi viene in genere presentato all'utente in una casella combinata o in un altro controllo dell'interfaccia utente che consente all'utente di selezionare il metodo desiderato.
    > [!Note]  
    > Il richiedente può scegliere di filtrare l'elenco di metodi visualizzato in base ai bit della proprietà del metodo indicati in **EAP \_ Method \_ info. eapProperties**. Alcuni metodi potrebbero non essere appropriati per le caratteristiche di sicurezza del trasporto fornito dal supplicant, ad esempio.

     

2.  Quando il controllo dell'interfaccia utente viene popolato con il set di possibili metodi EAP, l'utente seleziona il metodo che desidera configurare. In genere, il richiedente fornisce un pulsante **configurazione** o **Proprietà** per l'accesso dell'utente alle proprietà di configurazione del metodo EAP selezionato.
    > [!Note]
    > Il richiedente è consapevole del fatto che sono presenti proprietà configurabili dall'utente basate sul bit **eapPropSupportsConfig** abilitato nel **\_ metodo EAP \_ info. eapProperties**.
    >
    > Per ulteriori informazioni, vedere [**proprietà del metodo EAP**](eap-method-properties.md).

     

3.  Quando l'utente fa clic sul controllo dell'interfaccia utente appropriato, il richiedente chiama [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), passando nella funzione il valore **HWND** per l'interfaccia utente del richiedente, la struttura del [**\_ \_ tipo di metodo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) ottenuta dalla query alla struttura delle [**\_ \_ informazioni sul metodo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) e altri parametri obbligatori.
4.  La chiamata di [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) richiama l'interfaccia utente di configurazione di un metodo EAP. Al ritorno da **EapHostPeerInvokeConfigUI**, la funzione restituirà un BLOB di configurazione del metodo EAP come parametro out.
5.  Il richiedente archivia il BLOB di configurazione insieme alla struttura del [**\_ \_ tipo di metodo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) per l'uso con [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).
6.  Il metodo preciso per archiviare il BLOB Configuration è interamente fino al supplicant. Tuttavia, il richiedente deve sempre archiviare la configurazione in modo appropriato e sicuro per i dati di configurazione dell'autenticazione utente e del sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Abilitazione di Criteri di gruppo](enabling-group-policy.md)
</dt> <dt>

[Implementazione del supporto di In-Band NAP per i metodi EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementazione del supporto NAP per i metodi EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Trasferimento di dati tra i metodi supplicant e EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Supplicant EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




