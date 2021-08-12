---
description: Sicurezza dei componenti in coda
ms.assetid: 3fbeb81a-e3e4-495b-b891-896877fab92f
title: Sicurezza dei componenti in coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682a9b409df2f605c259a6af6741dcc6e59d9fc23852b950a13225b24386c010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547083"
---
# <a name="queued-components-security"></a>Sicurezza dei componenti in coda

Quando un client esegue una chiamata al metodo a un oggetto in coda, la chiamata viene effettivamente effettuata al registratore, che lo crea come parte di un messaggio al server. Il listener legge il messaggio dalla coda e lo passa al lettore. Il lettore richiama il componente server effettivo ed esegue la stessa chiamata al metodo . Il componente server deve osservare il contesto di chiamata di sicurezza del client (non il contesto di chiamata di sicurezza del giocatore) quando il giocatore effettua la chiamata al metodo. Il registratore effettua il marshalling del contesto di chiamata di sicurezza del client nel messaggio e il lettore lo annulla nel server prima di effettuare la chiamata al metodo. Per quanto riguarda l'oggetto server, non esiste alcuna differenza nel contesto di sicurezza tra una chiamata diretta dal client e una chiamata indiretta dal lettore. In particolare, i metodi richiamati vengono eseguiti con i privilegi del mittente.

Un componente in coda COM+ supporta la semantica di sicurezza basata sui ruoli proprio come altri componenti creati per l'uso con le applicazioni COM+. I componenti di un'applicazione in coda possono quindi usare interfacce a livello di codice per individuare l'appartenenza al ruolo del chiamante ([**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)) o un utente specifico ([**ISecurityCallContext::IsUserInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-isuserinrole)). È consigliabile che qualsiasi componente in coda con un potenziale impatto sulla sicurezza usi queste interfacce per controllare in modo esplicito le credenziali del mittente.

L'identità del chiamante è l'identità associata a una chiamata al metodo. L'identità del chiamante viene usata dalla sicurezza basata sui ruoli ed è presente nel contesto di chiamata di sicurezza. Nei componenti in coda l'identità del chiamante è rappresentata come dati nel messaggio di Accodamento messaggi. Accodamento messaggi autentica l'identità del mittente del messaggio. Quando l'identità del chiamante e l'identità del mittente del messaggio sono uguali, Accodamento messaggi autentica sia il messaggio che il chiamante. Questo è il caso consueto.

> [!Note]  
> I componenti in coda COM+ non supportano la sicurezza di tipo rappresentazione, che consente a un server di ottenere un token di accesso corrispondente all'identità client e usarlo per eseguire controlli di controllo di accesso o agire nel contesto di sicurezza client.

 

Quando il chiamante di un componente in coda interagisce con il componente tramite un registratore out-of-process, le identità del chiamante e del mittente del messaggio (registratore) possono essere diverse. In questo caso, i componenti in coda COM+ verificano che il mittente del messaggio sia membro del ruolo QC Trusted User nel server. Inoltre, il registratore out-of-process richiede un certificato di autenticazione perché viene autenticato da Accodamento messaggi.

Ai membri del ruolo QC Trusted User è consentito specificare un'identità arbitraria, il che significa che un membro malintenzionato potrebbe eseguire una chiamata al componente in coda con privilegi elevati. È quindi consigliabile che il numero di tali utenti sia mantenuto al minimo assoluto.

A causa del rischio di un attacco sofisticato associato a qualsiasi meccanismo che propaga l'identità in una rete, nonché del rischio di un semplice attacco Denial of Service causando l'inondazione delle code con richieste non eseguibili, è consigliabile distribuire il servizio componenti in coda COM+ solo in una rete di host attendibili, ad esempio  in una rete privata o in una rete privata virtuale o dietro un firewall configurato in modo appropriato.

I componenti in coda COM+ vengono eseguiti su DCOM, quindi è possibile proteggere l'integrità e il segreto  delle chiamate ai metodi  in coda selezionando **Privacy** pacchetti come impostazione Livello di autenticazione delle chiamate nella scheda Sicurezza della finestra Proprietà dell'applicazione in coda. 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza COM+](com--security.md)
</dt> <dt>

[Limitazioni di sicurezza in modalità gruppo di lavoro](security-limitations-in-workgroup-mode.md)
</dt> <dt>

[Specifica del protocollo di autenticazione](specifying-the-authentication-protocol.md)
</dt> </dl>

 

 



