---
title: Disattivazione della sicurezza delle chiamate
description: La sicurezza delle chiamate determina se un client dispone dell'autorizzazione per chiamare i metodi di un server. Esistono due modi per disabilitare la sicurezza delle chiamate, che prevede l'uso di Dcomcnfg.exe per modificare il registro di sistema, mentre l'altro richiede chiamate a CoInitializeSecurity.
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a838a9c7936c126a1fedeeafc977f55641b63c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395530"
---
# <a name="turning-off-call-security"></a>Disattivazione della sicurezza delle chiamate

La sicurezza delle chiamate determina se un client dispone dell'autorizzazione per chiamare i metodi di un server. Esistono due modi per disabilitare la sicurezza delle chiamate: uno prevede l'uso di Dcomcnfg.exe per modificare il registro di sistema, mentre l'altro richiede chiamate a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

-   [Disattivazione della sicurezza delle chiamate tramite DCOMCNFG](#turning-off-call-security-using-dcomcnfg)
-   [Disattivazione della sicurezza delle chiamate a livello di codice](#turning-off-call-security-programmatically)
-   [Argomenti correlati](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a>Disattivazione della sicurezza delle chiamate tramite DCOMCNFG

Per modificare il registro di sistema, è possibile disattivare la sicurezza delle chiamate utilizzando Dcomcnfg.exe. Tuttavia, l'utilizzo di Dcomcnfg.exe per disattivare la sicurezza funziona solo se il client e il server non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Questo perché quando viene chiamato **CoInitializeSecurity** , DCOM ignora le impostazioni del registro di sistema e usa i valori specificati in **CoInitializeSecurity** .

Per disattivare la sicurezza con Dcomcnfg.exe, sia il client che il server devono impostare i livelli di autenticazione su nessuno. È necessario completare i passaggi seguenti:

1.  Eseguire Dcomcnfg.exe.
2.  Nella pagina **applicazioni** selezionare l'applicazione che rappresenta il server. Fare clic sul pulsante delle **Proprietà** (o fare doppio clic sull'applicazione selezionata).
3.  Fare clic sulla scheda **General** (Generale).
4.  Nella casella di riepilogo **livello di autenticazione predefinito** selezionare **(nessuno)**.
5.  Per applicare le modifiche, fare clic sul pulsante **applica** . Tuttavia, le modifiche non vengono applicate a tutte le istanze in esecuzione dell'applicazione.
6.  Se il client viene visualizzato nell'elenco della pagina *applicazioni* , ripetere i passaggi da 2 a 5, scegliendo il client anziché il server per il passaggio 2. Fare quindi clic su **OK**. Se il client non è presente nell'elenco, è possibile eseguire una delle tre operazioni seguenti:
    -   È possibile impostare il livello di autenticazione del client su None a livello di computer utilizzando Dcomcnfg.exe. Vedere l'avviso e la procedura riportata di seguito.
    -   È possibile impostare il livello di autenticazione del client su None a livello di codice.
    -   È possibile creare una chiave [AppID](appid-key.md) per il client per indicare un livello di autenticazione None. (Vedere [impostazione della sicurezza Process-Wide tramite il registro di sistema](setting-processwide-security-through-the-registry.md)).

Per impostare il livello di autenticazione su None a livello di computer:

> [!Note]  
> L'impostazione del livello di autenticazione a livello di computer su None è estremamente non sicura.

 

1.  Eseguire Dcomcnfg.exe.
2.  Scegliere la scheda **proprietà predefinite** .
3.  Nella casella di riepilogo **livello di autenticazione predefinito** scegliere **(nessuno)**.
4.  Fare clic sul pulsante **OK** .

## <a name="turning-off-call-security-programmatically"></a>Disattivazione della sicurezza delle chiamate a livello di codice

Per disattivare la protezione delle chiamate a livello di codice, sia il client che il server devono chiamare **CoInitializeSecurity**, impostando il livello di autenticazione nel parametro *dwAuthnLevel* sul \_ \_ livello auth C AuthN \_ \_ .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Disattivazione della sicurezza di attivazione](turning-off-activation-security.md)
</dt> </dl>

 

 




