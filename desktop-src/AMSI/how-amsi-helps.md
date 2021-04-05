---
title: Come AMSI consente di difendersi dal malware
description: Gli sviluppatori di applicazioni possono partecipare attivamente a malware Defense. In particolare, è possibile proteggere i clienti da malware basati su script dinamici e da viali non tradizionali di cyberattack.
ms.topic: article
ms.date: 02/27/2019
ms.openlocfilehash: 0d6aee30034312073123f5ab14b1924fd01e6eac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708149"
---
# <a name="how-the-antimalware-scan-interface-amsi-helps-you-defend-against-malware"></a>Come l'interfaccia di analisi antimalware (AMSI) consente di difendersi dal malware

Per un'introduzione all'interfaccia di analisi antimalware di Windows (AMSI), vedere [interfaccia di analisi antimalware (AMSI)](antimalware-scan-interface-portal.md).

Gli sviluppatori di applicazioni possono partecipare attivamente a malware Defense. In particolare, è possibile proteggere i clienti da malware basati su script dinamici e da viali non tradizionali di cyberattack.

Per esempio, supponiamo che l'applicazione sia configurabile tramite script: accetta script arbitrari e lo esegue tramite un motore di script. Nel momento in cui uno script è pronto per essere fornito al motore di script, l'applicazione può chiamare le API di Windows AMSI per richiedere un'analisi del contenuto. In questo modo, è possibile determinare in modo sicuro se lo script è dannoso prima di decidere di procedere ed eseguirlo.

Questo vale anche se lo script è stato generato in fase di esecuzione. Lo script (dannoso o altro) può superare diversi passaggi di deoffuscamento. Tuttavia, è necessario fornire il motore di scripting con codice normale e non offuscato. Questo è il punto in cui vengono richiamate le API AMSI.

Di seguito è illustrata l'architettura AMSI, in cui l'applicazione è rappresentata da una delle caselle "altre applicazioni".

![architettura AMSI](images/AMSI7Archi.jpg)

L'interfaccia AMSI di Windows è aperta. Il che significa che qualsiasi applicazione può chiamarla; qualsiasi motore antimalware registrato può elaborare il contenuto inviato.

Non è necessario limitare la discussione ai motori di script. Probabilmente l'applicazione è un'app di comunicazione e analizza i messaggi istantanei per i virus prima che vengano visualizzati ai clienti. O forse il software è un gioco che convalida i plug-in prima di installarli. Sono disponibili numerose opportunità e scenari per l'uso di AMSI.

## <a name="amsi-in-action"></a>AMSI in azione

Diamo un'occhiata a AMSI in Action. In questo esempio, Windows Defender è l'applicazione che chiama le API AMSI. È tuttavia possibile chiamare le stesse API dall'interno dell'applicazione.

Di seguito è riportato un esempio di uno script che usa la tecnica di codifica XOR per nasconderne lo scopo, indipendentemente dal fatto che tale finalità sia benigna o meno. Per questa illustrazione, è possibile immaginare che lo script è stato scaricato da Internet.

![script di esempio codificato in base 64](images/AMSI8.png)

Per rendere le cose più interessanti, è possibile immettere questo script manualmente dalla riga di comando, in modo che non esista un file effettivo da monitorare. Questo mirroring è noto come "minaccia priva di file". Non è semplice come analizzare i file su disco. La minaccia potrebbe essere una backdoor che risiede solo nella memoria di un computer.

Di seguito viene visualizzato il risultato dell'esecuzione dello script in Windows PowerShell. Si noterà che Windows Defender è in grado di rilevare l'esempio di test AMSI in questo scenario complesso, usando semplicemente la firma di esempio di AMSI test standard.

![Windows Defender che rileva l'esempio di test di AMSI](images/AMSI9proper.png)

## <a name="amsi-integration-with-javascriptvba"></a>Integrazione di AMSI con JavaScript/VBA

Il flusso di lavoro illustrato di seguito descrive il flusso end-to-end di un altro esempio, in cui viene illustrata l'integrazione di AMSI con l'esecuzione della macro all'interno Microsoft Office.

![Integrazione di AMSI con JavaScript/VBA](images/integ-js-vba.png)

- L'utente riceve un documento contenente una macro (dannosa), che elude le analisi statiche del software antivirus mediante tecniche quali l'offuscamento, i file protetti da password o altro.
- L'utente apre quindi il documento che contiene la macro (dannosa). Se il documento viene aperto in visualizzazione protetta, l'utente fa clic su **Abilita modifica** per uscire dalla visualizzazione protetta.
- L'utente fa clic su **Abilita macro** per consentire l'esecuzione delle macro.
- Quando viene eseguita la macro, il runtime VBA usa un buffer circolare per registrare \[ 1 \] dato e i parametri correlati alle chiamate alle API Win32, com e VBA.
- Quando si osservano specifiche API Win32 o COM considerate a rischio elevato (noti anche come *trigger*) \[ 2 \] , l'esecuzione della macro viene interrotta e il contenuto del buffer circolare viene passato a AMSI.
- Il provider di servizi anti-malware AMSI registrato risponde con un verdetto per indicare se il comportamento della macro è dannoso o meno.
- Se il comportamento è non dannoso, l'esecuzione della macro continua.
- In caso contrario, se il comportamento è dannoso, Microsoft Office chiude la sessione in risposta all'avviso \[ 3 \] e l'AV può mettere in quarantena il file.

## <a name="what-does-this-mean-for-you"></a>Che cosa significa?

Per gli utenti di Windows, tutti i software dannosi che usano tecniche di offuscamento e evasione sugli host di scripting predefiniti di Windows 10 vengono controllati automaticamente a un livello più profondo che mai, garantendo livelli aggiuntivi di protezione.

Per gli sviluppatori di applicazioni, provare a fare in modo che l'applicazione chiami l'interfaccia AMSI di Windows se si vuole trarre vantaggio da (e proteggere i clienti con) analisi e analisi aggiuntive di contenuto potenzialmente dannoso.

Un fornitore di software antivirus può prendere in considerazione l'implementazione del supporto per l'interfaccia AMSI. Quando si esegue questa operazione, il motore avrà una visione più approfondita dei dati che le applicazioni (inclusi gli host di scripting predefiniti di Windows 10) considerano potenzialmente dannosi.

## <a name="more-background-info-about-fileless-threats"></a>Altre informazioni di base sulle minacce per i file

Per informazioni più dettagliate sui tipi di minacce informatiche che Windows AMSI è progettato per la difesa, potrebbe essere utile. In questa sezione si esaminerà il tradizionale gioco Cat-and-mouse che si svolge nell'ecosistema di malware.

Si userà PowerShell come esempio. Tuttavia, è possibile sfruttare le stesse tecniche e processi che verranno illustrati con qualsiasi linguaggio dinamico &mdash; VBScript, Perl, Python, Ruby e altro ancora.

Ecco un esempio di script di PowerShell dannoso.

![esempio di script di PowerShell dannoso](images/AMSI1.png)

Sebbene questo script scriva semplicemente un messaggio sullo schermo, malware è in genere più nefasto. Tuttavia, è possibile scrivere facilmente una firma per individuarla. Ad esempio, la firma potrebbe cercare la stringa "write-host ' pWnd!'" in qualsiasi file aperto dall'utente. Ottimo: il primo malware è stato rilevato.

Dopo essere stato rilevato dalla prima firma, tuttavia, gli autori di malware rispondono. Rispondono creando script dinamici come questo esempio.

![esempio di script dinamico](images/AMSI2.png)

In questo scenario, gli autori di malware creano una stringa che rappresenta lo script di PowerShell da eseguire. Ma usano una semplice tecnica di concatenazione di stringhe per suddividere la firma precedente. Se si visualizza l'origine di una pagina Web con carico elevato, si noterà che molte istanze di questa tecnica vengono usate per evitare il software di blocco ad.

Infine, l'autore del malware passa questa stringa concatenata `Invoke-Expression` al &mdash; meccanismo di PowerShell per il cmdlet per valutare gli script composti o creati in fase di esecuzione.

In risposta, il software antimalware inizia a eseguire l'emulazione del linguaggio di base. Se, ad esempio, sono presenti due stringhe concatenate, la concatenazione delle due stringhe viene emulata, quindi le firme vengono eseguite sul risultato. Sfortunatamente, si tratta di un approccio piuttosto fragile, perché i linguaggi tendono a offrire molti modi per rappresentare e concatenare le stringhe.

Quindi, dopo essere stata rilevata da questa firma, gli autori di malware passano a qualcosa di più complesso, &mdash; ad esempio, codificando il contenuto dello script in Base64, come nell'esempio seguente.

![esempio di contenuto di script in Base64](images/AMSI3.png)

In questo modo, la maggior parte dei motori antimalware implementano anche l'emulazione della decodifica Base64. Quindi, poiché viene implementata anche l'emulazione della decodifica Base64, l'esecuzione è più avanti.

In risposta, gli autori di malware passano all'offuscamento algoritmico, &mdash; ad esempio un semplice meccanismo di codifica XOR negli script che eseguono.

![esempio di script di offuscamento algoritmico](images/AMSI4.png)

A questo punto, in genere i motori antivirus verranno emulati o rilevati, pertanto non sarà necessario rilevare necessariamente le attività dello script. Tuttavia, è possibile iniziare a scrivere firme per le tecniche di offuscamento e codifica. In realtà, si tratta di un account che rappresenta la maggior parte delle firme per il malware basato su script.

Ma cosa accade se l'offuscatore è talmente semplice da avere un aspetto simile a quello di molti script ben funzionanti? Una firma per esso genera un numero inaccettabile di falsi positivi. Ecco uno script di *stage* di esempio troppo benigno per il rilevamento autonomo.

![uno script di staging di esempio troppo benigno per il rilevamento autonomo](images/AMSI5.png)

In questo esempio viene scaricata una pagina Web e viene richiamata parte del contenuto. Di seguito è riportato l'equivalente nello script Visual Basic.

![equivalente nello script Visual Basic](images/AMSI6.png)

Ciò che peggiora in entrambi questi esempi è che il motore antivirus controlla i file aperti dall'utente. Se il contenuto dannoso risiede solo in memoria, l'attacco potrebbe non essere rilevato.

In questa sezione sono state illustrate le limitazioni del rilevamento tramite firme tradizionali. Tuttavia, anche se uno script dannoso può passare attraverso diversi passaggi di deoffuscamento, è necessario fornire al motore di script un codice semplice e non offuscato. A questo punto &mdash; , come descritto nella prima sezione sopra &mdash; gli host di scripting predefiniti di Windows 10, chiamare le API AMSI per richiedere un'analisi di questo contenuto non protetto. E l'applicazione può eseguire la stessa operazione.

## <a name="related-resources"></a>Risorse correlate

* [Minacce per i file](/windows/security/threat-protection/intelligence/fileless-threats)
* [Office VBA + AMSI: parte del velo sulle macro dannose](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/12/office-vba-amsi-parting-the-veil-on-malicious-macros/)
* [Non visibile, ma non invisibile: la sconfitta di malware senza file con monitoraggio del comportamento, AMSI e Next-gen AV](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/27/out-of-sight-but-not-invisible-defeating-fileless-malware-with-behavior-monitoring-amsi-and-next-gen-av/)
