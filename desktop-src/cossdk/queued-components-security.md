---
description: Sicurezza dei componenti in coda
ms.assetid: 3fbeb81a-e3e4-495b-b891-896877fab92f
title: Sicurezza dei componenti in coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b51592f6216d7380e877f2cd582a277f1583b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127142"
---
# <a name="queued-components-security"></a>Sicurezza dei componenti in coda

Quando un client effettua una chiamata al metodo in un oggetto in coda, la chiamata viene effettivamente effettuata al registratore, che lo inserisce come parte di un messaggio al server. Il listener legge il messaggio dalla coda e lo passa al lettore. Il lettore richiama il componente server effettivo ed effettua la stessa chiamata al metodo. Il componente server deve osservare il contesto di chiamata di sicurezza del client (non il contesto di chiamata di sicurezza del giocatore) quando il giocatore effettua la chiamata al metodo. Il registratore esegue il marshalling del contesto di chiamata di sicurezza del client nel messaggio e il giocatore ne esegue l'unmarshalling sul server prima di effettuare la chiamata al metodo. Per quanto riguarda l'oggetto server, non esiste alcuna differenza nel contesto di sicurezza tra una chiamata diretta dal client e una chiamata indiretta da parte del lettore. In particolare, i metodi richiamati Execute con i privilegi del mittente.

Un componente COM+ accodato supporta la semantica di sicurezza basata sui ruoli come gli altri componenti creati per l'utilizzo con le applicazioni COM+. I componenti di un'applicazione in coda possono pertanto utilizzare interfacce programmatiche per individuare l'appartenenza al ruolo del chiamante ([**ISecurityCallContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)) o un utente specifico ([**ISecurityCallContext:: IsUserInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-isuserinrole)). È consigliabile che tutti i componenti in coda con un potenziale impatto sulla sicurezza usino queste interfacce per controllare in modo esplicito le credenziali del mittente.

L'identità del chiamante è l'identità associata a una chiamata al metodo. L'identità del chiamante viene utilizzata dalla sicurezza basata sui ruoli ed è presente nel contesto della chiamata di sicurezza. Nei componenti in coda, l'identità del chiamante viene rappresentata come dati nel messaggio di Accodamento messaggi. Accodamento messaggi autentica l'identità del mittente del messaggio. Quando l'identità del chiamante e l'identità del mittente del messaggio sono le stesse, Accodamento messaggi autentica sia il messaggio che il chiamante. Questo è il caso usuale.

> [!Note]  
> I componenti COM+ in coda non supportano la sicurezza in stile di rappresentazione, che consente a un server di ottenere un token di accesso corrispondente all'identità del client e usarlo per eseguire controlli di controllo di accesso o per agire nel contesto di sicurezza del client.

 

Quando il chiamante di un componente in coda interagisce con il componente tramite una registrazione out-of-process, le identità del chiamante e del mittente del messaggio (registratore) possono essere diverse. In questo caso, i componenti in coda COM+ verificano che il mittente del messaggio sia un membro del ruolo utente attendibile QC sul server. Inoltre, la registrazione out-of-process richiede un certificato di autenticazione perché viene autenticato da Accodamento messaggi.

Ai membri del ruolo utente attendibile QC è consentito specificare un'identità arbitraria, il che significa che un membro malintenzionato potrebbe eseguire una chiamata di componente in coda con privilegi elevati. È quindi consigliabile che il numero di tali utenti venga mantenuto come minimo assoluto.

A causa del rischio di un attacco sofisticato associato a qualsiasi meccanismo che propaga l'identità in una rete, nonché il rischio di un attacco di tipo Denial of Service semplice tramite l'alluvione delle code con richieste non eseguibili, si consiglia di distribuire il servizio componenti in coda COM+ solo in una rete di host attendibili, ad esempio in una rete privata o in una rete privata virtuale o dietro un firewall configurato in modo appropriato.

I componenti COM+ in coda vengono eseguiti su DCOM, quindi è possibile proteggere l'integrità e la segretezza delle chiamate ai metodi in coda selezionando la **privacy dei pacchetti** come **livello di autenticazione delle chiamate** impostazione nella scheda **sicurezza** della finestra delle **Proprietà** dell'applicazione in coda.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza COM+](com--security.md)
</dt> <dt>

[Limitazioni di sicurezza in modalità gruppo di lavoro](security-limitations-in-workgroup-mode.md)
</dt> <dt>

[Specifica del protocollo di autenticazione](specifying-the-authentication-protocol.md)
</dt> </dl>

 

 



