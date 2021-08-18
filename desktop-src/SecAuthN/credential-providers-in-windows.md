---
description: Provider di credenziali in Windows 10
ms.assetid: BCF69196-D4E4-41D0-B372-5000FD50164B
title: Provider di credenziali in Windows 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38543127709007407c013a2a8ff047f7c91f4440351653061e894f4e7c2d90d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008799"
---
# <a name="credential-providers-in-windows-10"></a>Provider di credenziali in Windows 10

I provider di credenziali sono il meccanismo principale per l'autenticazione utente. Attualmente sono l'unico metodo per dimostrare la propria identità necessaria per l'accesso e altri scenari di autenticazione del sistema. Con Windows 10 e l'introduzione di Microsoft Passport, i provider di credenziali sono più importanti che mai; verranno usati per l'autenticazione in app, siti Web e altro ancora.

Microsoft offre un'ampia gamma di provider di credenziali come parte di Windows, ad esempio password, PIN, smart card e Windows Hello (riconoscimento di impronta digitale, viso e Iris). Questi provider sono definiti "provider di credenziali di sistema" in questo articolo. Gli OEM, le aziende e altre entità possono scrivere i propri provider di credenziali e integrarli facilmente in Windows. Questi provider sono definiti "provider di credenziali di terze parti" in questo articolo. Si noti che i provider di credenziali V1 e V2 sono supportati in Windows 10. È importante che gli autori e i responsabili dei provider di credenziali di terze parti comprendano queste raccomandazioni.

## <a name="system-credential-providers"></a>Provider di credenziali di sistema

È consigliabile che sia sempre disponibile almeno un provider di credenziali di sistema per ogni utente nel dispositivo oltre a qualsiasi provider di credenziali di terze parti. Inoltre, durante la configurazione del provider di credenziali di terze parti, a ogni utente del dispositivo deve essere richiesto di configurare almeno un provider di credenziali di sistema (se non sono disponibili altre opzioni di ripristino; vedere Scenario A, di seguito).

### <a name="scenario-a"></a>Scenario A

Un utente dell'account locale ha configurato un provider di credenziali di terze parti e lo usa regolarmente per accedere al dispositivo. Un giorno, l'utente installa alcuni aggiornamenti nel dispositivo che interrompe il provider di credenziali di terze parti e l'utente non è a conoscenza di questa modifica prima di riavviare il computer.

Al riavvio successivo, l'utente si trova nella schermata di accesso e non è in grado di usare il provider di credenziali di terze parti previsto. Se l'utente ha configurato un provider di credenziali di sistema, l'utente potrà accedere al computer usandolo. In caso contrario, l'utente non può recuperare l'account nel computer.

### <a name="scenario-b"></a>Scenario B

Un utente dell'account MSA/AD/AAD ha configurato un provider di credenziali di terze parti e lo usa regolarmente per accedere al dispositivo. Un giorno, l'utente installa alcuni aggiornamenti nel dispositivo che interrompe il provider di credenziali di terze parti e l'utente non è a conoscenza di questa modifica prima di riavviare il computer.

Al riavvio successivo, l'utente si trova nella schermata di accesso e non è in grado di usare il provider di credenziali di terze parti previsto. Se l'utente ha configurato un provider di credenziali di sistema, l'utente potrà accedere al computer usandolo. In alternativa, se il provider di credenziali password del sistema è disponibile, l'utente può richiedere/reimpostare in remoto la password e usarla per accedere al computer. Se nessuna delle due opzioni è disponibile, l'utente non può recuperare l'account nel computer.

### <a name="conclusion"></a>Conclusione

In sintesi, si vuole sconsigliare la disabilitazione di tutti i provider di credenziali di sistema in un dispositivo. Anche se i provider di credenziali di terze parti possono soddisfare requisiti di autenticazione aggiuntivi per determinati gruppi di utenti, è molto importante assicurarsi che l'utente possa sempre ottenere nuovamente l'accesso al computer quando si verifica una modifica di rilievo. I provider di credenziali di sistema offrono questa garanzia.

## <a name="custom-credential-providers"></a>Provider di credenziali personalizzati

Il framework Windows provider di credenziali consente agli sviluppatori di creare provider di credenziali personalizzati. Quando [Winlogon vuole raccogliere](winlogon.md) le credenziali, l'interfaccia utente di accesso esegue una query su ogni provider di credenziali per il numero di credenziali da enumerare. Dopo che tutti i provider hanno enumerato i riquadri, l'interfaccia utente di accesso li visualizza all'utente. L'utente interagisce quindi con un riquadro per fornire le credenziali necessarie. L'interfaccia utente di accesso invia queste credenziali per l'autenticazione. I provider di credenziali possono essere usati anche dall'interfaccia utente delle credenziali quando sono necessarie le credenziali. Per un elenco di scenari in cui è possibile supporto di un provider di credenziali, vedere [**\_ \_ \_ SCENARIO**](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario) DI UTILIZZO DEL PROVIDER DI CREDENZIALI.

Grazie a questo sistema, è molto più facile creare un provider di credenziali rispetto a quanto non fosse in origine. Gran parte del lavoro viene gestito dalla combinazione di [Winlogon](winlogon.md), l'interfaccia utente di accesso e l'interfaccia utente delle credenziali. A tale scopo, è necessario creare un'implementazione personalizzata di [**ICredentialProvider**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider) e [**ICredentialProviderCredential.**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential) Se si implementa un provider di credenziali V2, consigliato, è necessario implementare [**anche ICredentialProviderCredential2.**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential2)

È importante notare che i provider di credenziali non sono meccanismi di imposizione. Vengono semplicemente usati per raccogliere e serializzare le credenziali, inviandole per l'autorizzazione. L'autorità locale e i pacchetti di autenticazione gestiranno ed eventuali imposizioni di sicurezza necessarie.

Combinando i provider di credenziali con l'hardware supportato, è possibile estendere Windows per supportare l'accesso con informazioni biometriche, password, PIN, certificati smart card o qualsiasi pacchetto di autenticazione personalizzato che si sceglie di creare. È possibile personalizzare l'esperienza di accesso per l'utente anche in diversi modi. Ad esempio, quando l'interfaccia utente di accesso esegue una query sul provider di credenziali per i riquadri delle credenziali, è possibile specificare un riquadro predefinito per fornire un'esperienza personalizzata per un utente. I provider di credenziali possono anche essere progettati per supportare l'accesso Single Sign-On (SSO), l'autenticazione degli utenti a un punto di accesso sicuro e l'accesso al computer.

I provider di credenziali vengono registrati in Windows computer e sono responsabili di quanto segue.

-   Descrizione delle informazioni sulle credenziali necessarie per l'autenticazione.
-   Gestione della comunicazione e della logica con qualsiasi autorità di autenticazione esterna.
-   Creazione del pacchetto delle credenziali per l'accesso interattivo e di rete.

> [!TIP]
>
> Tenere presente che è possibile installare più provider di credenziali in un singolo computer.

## <a name="wrapping-credential-providers"></a>Wrapping dei provider di credenziali

È possibile eseguire il wrapping di un provider di credenziali di sistema per aggiungere funzionalità al provider di credenziali non supportato in modo nativo. Questa operazione non è consigliata perché può causare un comportamento problematico. È possibile apportare modifiche al provider di credenziali che potrebbero essere in conflitto con il wrapper causando un'esperienza utente scadente o persino impedendo all'utente di accedere al dispositivo. Ciò vale soprattutto per la frequenza di aggiornamento Windows 10.

Se è necessaria una funzionalità in un provider di credenziali non inclusa in modo nativo, il percorso consigliato è creare un provider di credenziali personalizzato. Si tratta di un approccio più stabile che non accetta dipendenze dai provider di sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider di credenziali di accesso Windows guidata](https://go.microsoft.com/fwlink/?LinkId=717287)
</dt> <dt>

[ICredentialProvider](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider)
</dt> <dt>

[SERIALIZZAZIONE \_ DELLE CREDENZIALI DEL PROVIDER DI \_ \_ CREDENZIALI](/windows/desktop/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization)
</dt> <dt>

[SCENARIO DI \_ UTILIZZO DEL PROVIDER DI \_ \_ CREDENZIALI](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario)
</dt> </dl>

 

 
