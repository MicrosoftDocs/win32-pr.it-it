---
title: Disattivazione della sicurezza di attivazione
description: Disattivazione della sicurezza di attivazione
ms.assetid: 3474f8ad-f041-4886-ad39-ff0603c5c69e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da3ebd7cc03d79fc38fbafe3bc652efc3499437
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399768"
---
# <a name="turning-off-activation-security"></a>Disattivazione della sicurezza di attivazione

In genere, l'attivazione Usa impostazioni di sicurezza predefinite. Tuttavia, è possibile controllare la sicurezza dell'attivazione specificando una struttura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) , che è un membro della struttura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) che viene passata alle funzioni di attivazione. Se il client specifica un livello di autenticazione di \_ un \_ livello auth C AuthN \_ \_ nella struttura **COAUTHINFO** , non viene eseguito alcun tentativo di autenticazione. In caso contrario, viene tentata l'attivazione sicura e, se l'autenticazione non riesce, l'attivazione non riesce.

Se il client non specifica una struttura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) esplicita e imposta invece il puntatore su **null**, com tenterà di autenticare il client. Se non è in grado di autenticare il client, COM controlla il descrittore di sicurezza dell'autorizzazione Launch per verificare se è presente un DACL **null** o un ACL che consente l'accesso a tutti gli utenti. Se il controllo ha esito positivo, viene avviato il server. Pertanto, anche se il client non specifica una struttura **COAUTHINFO**, l'attivazione non sicura potrebbe verificarsi quando il server lo consente.

> [!Note]  
> Per consentire agli utenti di rete non autenticati di eseguire un'applicazione COM, i ruoli applicazione devono includere l'utente anonimo. A partire da Windows Server 2003, per impostazione predefinita, l'utente anonimo non è incluso nel gruppo Everyone.

 

Perché un client desidera disattivare la sicurezza dell'attivazione in modo esplicito anche se l'attivazione non sicura verrà eseguita se il server lo consente? Poiché la disattivazione esplicita della sicurezza dell'attivazione aumenta le prestazioni quando il client non desidera o non necessita di controlli di sicurezza.

Per disattivare esplicitamente la sicurezza di attivazione, è necessario eseguire le operazioni seguenti:

-   Il client deve specificare un livello di autenticazione del \_ \_ livello auth C AuthN \_ \_ nella struttura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) che è un membro della struttura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) fornita alla funzione Activation.
-   Il client deve specificare un livello di rappresentazione di RPC \_ C \_ Imp \_ level \_ Impersonate nella struttura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) che è un membro della struttura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) fornita alla funzione Activation. Se questo valore non viene passato, si otterrà il \_ server RPC \_ non \_ disponibile.
-   Il server deve specificare **tutti gli utenti** per le **autorizzazioni di avvio predefinite**. Il metodo consigliato per eseguire questa attività consiste nell'usare Dcomcnfg.exe come indicato di seguito:
    1.  Eseguire Dcomcnfg.exe.
    2.  Nella pagina **applicazioni** selezionare l'applicazione che rappresenta il server. Fare clic sul pulsante delle **Proprietà** (o fare doppio clic sull'applicazione selezionata).
    3.  Nella pagina delle proprietà **sicurezza** , fare clic sul pulsante **Usa autorizzazioni di avvio personalizzate** .
    4.  Fare clic sul pulsante **modifica** nell'area **autorizzazioni di avvio** .
    5.  Nella finestra di dialogo **autorizzazioni valore registro di sistema** fare clic sul pulsante **Aggiungi** .
    6.  Selezionare la voce **tutti** nella casella di riepilogo.
    7.  Nella casella **di riepilogo tipo di accesso** scegliere **Consenti avvio**.
    8.  Fare clic sul pulsante **OK** .

> [!Note]  
> In Windows Server 2003, la funzionalità di autenticazione per l'applicazione di sistema COM+ include il valore EOAC \_ Disable \_ AAA. Questo valore, che disabilita le attivazioni di Activate-As-Activator (AAA), viene usato nella chiamata [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) quando viene avviata l'applicazione di sistema. Impostando la funzionalità di autenticazione su EOAC \_ Disable AAA è possibile consentire a \_ un'applicazione in esecuzione con un account con privilegi, ad esempio LocalSystem, di impedire l'utilizzo dell'identità per l'avvio di componenti non attendibili.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Disattivazione della sicurezza delle chiamate](turning-off-call-security.md)
</dt> </dl>

 

 