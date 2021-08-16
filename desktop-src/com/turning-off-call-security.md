---
title: Disattivazione della sicurezza delle chiamate
description: La sicurezza delle chiamate determina se un client dispone dell'autorizzazione per chiamare i metodi di un server. Esistono due modi per disabilitare la sicurezza delle chiamate Uno prevede l'uso di Dcomcnfg.exe per modificare il Registro di sistema e l'altro richiede chiamate a CoInitializeSecurity.
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d8d8f4a48baed00655761e89a12f0aa84846a0a2defdc0b2e444b2bee9103f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550565"
---
# <a name="turning-off-call-security"></a>Disattivazione della sicurezza delle chiamate

La sicurezza delle chiamate determina se un client dispone dell'autorizzazione per chiamare i metodi di un server. Esistono due modi per disabilitare la sicurezza delle chiamate: uno prevede l'uso di Dcomcnfg.exe per modificare il Registro di sistema e l'altro richiede chiamate a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

-   [Disattivazione della sicurezza delle chiamate tramite DCOMCNFG](#turning-off-call-security-using-dcomcnfg)
-   [Disattivazione della sicurezza delle chiamate a livello di codice](#turning-off-call-security-programmatically)
-   [Argomenti correlati](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a>Disattivazione della sicurezza delle chiamate tramite DCOMCNFG

La sicurezza delle chiamate può essere disattivata più facilmente usando Dcomcnfg.exe per modificare il Registro di sistema. Tuttavia, l'Dcomcnfg.exe per disattivare la sicurezza funzionerà solo se sia il client che il server non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Questo perché quando viene chiamato **CoInitializeSecurity,** DCOM ignora le impostazioni del Registro di sistema e usa invece i valori forniti a **CoInitializeSecurity.**

Per disattivare la sicurezza con Dcomcnfg.exe, sia il client che il server devono impostare i livelli di autenticazione su Nessuno. È necessario completare i passaggi seguenti:

1.  Eseguire Dcomcnfg.exe.
2.  Nella pagina **Applicazioni** selezionare l'applicazione che rappresenta il server. Fare clic **sul pulsante** Proprietà oppure fare doppio clic sull'applicazione selezionata.
3.  Fare clic sulla scheda **General** (Generale).
4.  Nella casella **di riepilogo Livello di** autenticazione predefinito selezionare **(Nessuno)**.
5.  Fare clic **sul pulsante** Applica per applicare le modifiche. Tuttavia, le modifiche non vengono applicate alle istanze in esecuzione dell'applicazione.
6.  Se il client viene visualizzato nell'elenco nella pagina *Applicazioni,* ripetere i passaggi da 2 a 5, scegliendo il client anziché il server per il passaggio 2. Fare quindi clic su **OK**. Se il client non è in elenco, è possibile eseguire una delle tre operazioni seguenti:
    -   È possibile impostare il livello di autenticazione del client su Nessuno a livello di computer usando Dcomcnfg.exe. Vedere l'avviso e la procedura seguente.
    -   È possibile impostare il livello di autenticazione del client su Nessuno a livello di codice.
    -   È possibile creare una [chiave AppID](appid-key.md) per il client per indicare un livello di autenticazione None. Vedere [Impostazione della Process-Wide sicurezza tramite il Registro di sistema.](setting-processwide-security-through-the-registry.md)

Per impostare il livello di autenticazione su Nessuno a livello di computer:

> [!Note]  
> L'impostazione del livello di autenticazione a livello di computer su Nessuno è estremamente non sicura.

 

1.  Eseguire Dcomcnfg.exe.
2.  Scegliere la **scheda Proprietà** predefinite.
3.  Nella casella **di riepilogo Livello di** autenticazione predefinito scegliere **(Nessuno).**
4.  Fare clic sul pulsante **OK** .

## <a name="turning-off-call-security-programmatically"></a>Disattivazione della sicurezza delle chiamate a livello di codice

Per disattivare la sicurezza delle chiamate a livello di codice, sia il client che il server devono chiamare **CoInitializeSecurity**, impostando il livello di autenticazione nel *parametro dwAuthnLevel* su RPC \_ C \_ AUTHN \_ LEVEL \_ NONE.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Disattivazione della sicurezza dell'attivazione](turning-off-activation-security.md)
</dt> </dl>

 

 




