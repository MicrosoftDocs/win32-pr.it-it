---
description: Provider di credenziali in Windows 10
ms.assetid: BCF69196-D4E4-41D0-B372-5000FD50164B
title: Provider di credenziali in Windows 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a7947000e5d5a989f71dcdddd808a8e1d5ab3f
ms.sourcegitcommit: cd9672511263d04c0e4bc41758dd1d9e89ea92b4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2021
ms.locfileid: "104350826"
---
# <a name="credential-providers-in-windows-10"></a>Provider di credenziali in Windows 10

I provider di credenziali rappresentano il meccanismo principale per l'autenticazione utente, attualmente sono l'unico metodo per gli utenti per dimostrare la propria identità, necessaria per l'accesso e altri scenari di autenticazione del sistema. Con Windows 10 e l'introduzione di Microsoft Passport, i provider di credenziali sono più importanti che mai. verranno usati per l'autenticazione in app, siti Web e altro ancora.

Microsoft offre un'ampia gamma di provider di credenziali come parte di Windows, ad esempio password, PIN, smart card e Windows Hello (impronta digitale, viso e iride). Questi sono detti "provider di credenziali di sistema" in questo articolo. Gli OEM, le aziende e altre entità possono scrivere i propri provider di credenziali e integrarli facilmente in Windows. Questi sono detti "provider di credenziali di terze parti" in questo articolo. Si noti che i provider di credenziali V1 e V2 sono supportati in Windows 10. È importante per gli autori e i manager dei provider di credenziali di terze parti comprendere questi consigli.

## <a name="system-credential-providers"></a>Provider di credenziali di sistema

È consigliabile che sia sempre disponibile almeno un provider di credenziali di sistema per ogni utente del dispositivo, oltre a qualsiasi provider di credenziali di terze parti. Inoltre, durante la configurazione del provider di credenziali di terze parti, a ogni utente del dispositivo deve essere richiesto di impostare almeno un provider di credenziali di sistema (se non sono disponibili altre opzioni di ripristino; vedere lo scenario A, riportato di seguito).

### <a name="scenario-a"></a>Scenario A

Un utente dell'account locale ha configurato un provider di credenziali di terze parti e lo usa regolarmente per accedere al dispositivo. Un giorno, l'utente installa un aggiornamento al dispositivo che interrompe il provider di credenziali di terze parti e l'utente non è a conoscenza di questa modifica prima di riavviare il computer.

Al successivo riavvio, l'utente si trova nella schermata di accesso e non è in grado di utilizzare il provider di credenziali di terze parti previsto. Se l'utente ha configurato un provider di credenziali di sistema, l'utente potrà accedere al computer usandolo. In caso contrario, l'utente non è in grado di ripristinare l'account nel computer.

### <a name="scenario-b"></a>Scenario B

Un utente dell'account MSA/AD/AAD ha configurato un provider di credenziali di terze parti e lo usa regolarmente per accedere al dispositivo. Un giorno, l'utente installa un aggiornamento al dispositivo che interrompe il provider di credenziali di terze parti e l'utente non è a conoscenza di questa modifica prima di riavviare il computer.

Al successivo riavvio, l'utente si trova nella schermata di accesso e non è in grado di utilizzare il provider di credenziali di terze parti previsto. Se l'utente ha configurato un provider di credenziali di sistema, l'utente potrà accedere al computer usandolo. In alternativa, se il provider di credenziali password del sistema è disponibile, l'utente può richiedere o reimpostare la password in remoto e usarla per accedere al computer. Se nessuna delle due opzioni è disponibile, l'utente non ha modo di recuperare l'account nel computer.

### <a name="conclusion"></a>Conclusione

In breve, si vuole scoraggiare la disabilitazione di tutti i provider di credenziali di sistema in un dispositivo. Sebbene i provider di credenziali di terze parti possano soddisfare requisiti di autenticazione aggiuntivi per determinati gruppi di utenti, è molto importante assicurarsi che l'utente possa sempre riottenere l'accesso al computer quando si verifica una modifica di rilievo. I provider di credenziali di sistema forniscono questa garanzia.

## <a name="custom-credential-providers"></a>Provider di credenziali personalizzati

Il Framework del provider di credenziali Windows consente agli sviluppatori di creare provider di credenziali personalizzati. Quando [Winlogon](winlogon.md) vuole raccogliere le credenziali, l'interfaccia utente di accesso esegue una query su ogni provider di credenziali per il numero di credenziali che desidera enumerare. Dopo che tutti i provider hanno enumerato i riquadri, l'interfaccia utente di accesso li visualizza all'utente. L'utente interagisce quindi con un riquadro per fornire le credenziali necessarie. L'interfaccia utente di accesso Invia le credenziali per l'autenticazione. I provider di credenziali possono anche essere usati dall'interfaccia utente delle credenziali quando sono necessarie le credenziali. Vedere [**\_ scenario di \_ utilizzo \_ del provider di credenziali**](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario) per un elenco di scenari in cui è possibile supportare un provider di credenziali.

Grazie a questo sistema, è molto più semplice creare un provider di credenziali piuttosto che in passato. Gran parte del lavoro viene gestita dalla combinazione di [Winlogon](winlogon.md), dell'interfaccia utente di accesso e dell'interfaccia utente delle credenziali. A tale scopo, sarà necessario creare un'implementazione personalizzata di [**ICredentialProvider**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider) e [**ICredentialProviderCredential**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential). Se si implementa un provider di credenziali V2, che è consigliato, sarà necessario implementare anche [**ICredentialProviderCredential2**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential2).

È importante notare che i provider di credenziali non sono meccanismi di imposizione. Vengono semplicemente utilizzati per raccogliere e serializzare le credenziali, che le inviano per l'autorizzazione. L'autorità locale e i pacchetti di autenticazione gestiranno ed eventuali imposizione di sicurezza necessaria.

Combinando i provider di credenziali con hardware supportato, è possibile estendere Windows per supportare l'accesso con informazioni biometriche, password, pin, certificati smart card o qualsiasi pacchetto di autenticazione personalizzato che si sceglie di creare. È possibile personalizzare l'esperienza di accesso per l'utente in diversi modi. Ad esempio, quando l'interfaccia utente di accesso esegue una query sul provider di credenziali per i riquadri delle credenziali, è possibile specificare un riquadro predefinito per offrire un'esperienza personalizzata per un utente. I provider di credenziali possono anche essere progettati per supportare single sign-on (SSO), per autenticare gli utenti a un punto di accesso sicuro e per l'accesso al computer.

I provider di credenziali sono registrati in un computer Windows e sono responsabili di quanto segue.

-   Descrizione delle informazioni sulle credenziali necessarie per l'autenticazione.
-   Gestione della comunicazione e della logica con le autorità di autenticazione esterne.
-   Creazione del pacchetto delle credenziali per l'accesso interattivo e di rete.

> [!TIP]
>
> Tenere presente che è possibile installare più provider di credenziali in un singolo computer.

## <a name="wrapping-credential-providers"></a>Wrapping di provider di credenziali

Per aggiungere funzionalità a tale provider di credenziali non supportato in modo nativo, è possibile eseguire il wrapping di un provider di credenziali di sistema. Questa operazione non è consigliata perché può causare un comportamento problematico. È possibile apportare modifiche al provider di credenziali che possono entrare in conflitto con il wrapper causando un'esperienza utente insufficiente o addirittura impedendo all'utente di accedere al dispositivo. Questa operazione è particolarmente vera con la cadenza frequente degli aggiornamenti di Windows 10.

Se è necessaria la funzionalità in un provider di credenziali che non è incluso in modalità nativa, il percorso consigliato consiste nel creare un provider di credenziali personalizzato. Si tratta di un approccio più stabile che non accetta dipendenze dai provider di sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esperienza di accesso di Windows basata su provider di credenziali](https://go.microsoft.com/fwlink/?LinkId=717287)
</dt> <dt>

[ICredentialProvider](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider)
</dt> <dt>

[\_ \_ serializzazione delle credenziali del provider di credenziali \_](/windows/desktop/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization)
</dt> <dt>

[\_scenario di \_ utilizzo del provider di credenziali \_](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario)
</dt> </dl>

 

 
