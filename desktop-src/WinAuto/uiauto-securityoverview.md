---
title: Considerazioni sulla sicurezza per le tecnologie per l'accesso facilitato
description: Le tecnologie per l'accesso facilitato sono applicazioni eseguite sul desktop di Windows e consentono agli utenti di accedere all'accessibilità di interagire con il sistema operativo e altre applicazioni in esecuzione nel computer, incluse le applicazioni nella nuova interfaccia utente di Windows.
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- attributo uiAccess
- Automazione interfaccia utente, attributo uiAccess
- sicurezza, attributo uiAccess
- Tag requestedExecutionLevel
- Automazione interfaccia utente, tag requestedExecutionLevel
- Automazione interfaccia utente, considerazioni sulla sicurezza
- Automazione interfaccia utente, file manifesto
- file manifesto
- controllo dell'account utente
- sicurezza, controllo dell'account utente
- sicurezza, file manifesto
- sicurezza, tag requestedExecutionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f2f5cf006c0adaf9b170a4ed11abd9afd52012
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2020
ms.locfileid: "106300641"
---
# <a name="security-considerations-for-assistive-technologies"></a>Considerazioni sulla sicurezza per le tecnologie per l'accesso facilitato

Le tecnologie per l'accesso facilitato sono applicazioni eseguite sul desktop di Windows e consentono agli utenti di accedere all'accessibilità di interagire con il sistema operativo e altre applicazioni in esecuzione nel computer, incluse le applicazioni nella nuova interfaccia utente di Windows. Le applicazioni di Assistive Technology funzionano recuperando le informazioni dal sistema operativo e da altre applicazioni, quindi presentando le informazioni in modo che siano accessibili all'utente. Un'applicazione di Assistive Technology può anche "guidare" a livello di codice il sistema operativo e altre applicazioni in base all'input dell'utente.

La natura delle applicazioni per la tecnologia per l'accessibilità richiede il superamento dei limiti del processo e l'accesso ai processi che vengono eseguiti a un livello di integrità superiore (IL). Un'applicazione per la tecnologia per l'accessibilità viene eseguita a media IL. Ad esempio, quando l'utente tenta di eseguire un'attività che richiede privilegi amministrativi, Windows visualizza una finestra di dialogo in cui viene chiesto all'utente di fornire il consenso per continuare. Questa finestra di dialogo viene eseguita con un livello di integrità superiore per proteggerla dalla comunicazione tra processi, in modo che IL software dannoso non possa simulare l'input dell'utente. Analogamente, la schermata di accesso al desktop viene eseguita con un livello di integrità superiore per impedire l'accesso da parte di altri processi.

In genere, le applicazioni di Assistive Technology necessitano dell'accesso agli elementi dell'interfaccia utente del sistema protetto o ad altri processi che potrebbero essere in esecuzione a un livello di privilegi più elevato. Pertanto, le applicazioni di Assistive Technology devono essere considerate attendibili dal sistema e devono essere eseguite con privilegi speciali.

Per ottenere l'accesso a processi IL più elevati, un'applicazione di Assistive Technology deve impostare il flag UIAccess nel manifesto dell'applicazione ed essere avviata da un utente con privilegi di amministratore.

> [!NOTE]
> I privilegi di accesso sono limitati come segue:
>
> - Un'applicazione che non dispone di UIAccess nel manifesto inizia con IL media IL e non può accedere all'interfaccia utente del processo con privilegi elevati ("medium +" IL).
> - Un'applicazione con UIAccess nel manifesto e avviata da un utente non appartenente al gruppo Administrators, viene avviata come IL "medio +" e non può accedere all'interfaccia utente con privilegi elevati (nessun elemento in esecuzione come "alto", ad esempio le app avviate tramite un **clic con il pulsante destro del mouse su > eseguito come amministratore**).
> - Un'applicazione dispone di accesso all'interfaccia utente e viene avviata da un utente amministratore avviata come IL "alto" e può accedere all'interfaccia utente con privilegi elevati perché ha lo stesso linguaggio IL.
>
> UIAccess non è sufficiente per consentire a un processo di spostarsi verso l'alto attraverso il limite IL.

Oltre ad accedere ai processi IL più elevati, un'applicazione di Assistive Technology con questi privilegi può essere eseguita come applicazione in primo piano nell'ordine z in qualsiasi momento, vale a dire che un'applicazione Assistive Technology può essere visibile e disponibile ogni volta che l'utente lo richiede.

> [!Important]
> Nessuno degli scenari precedentemente elencati fornisce l'accesso all'interfaccia utente in esecuzione nel sistema IL. Questa operazione è possibile solo se il processo viene avviato nel desktop del controllo dell'account utente (UAC) in SYSTEM (e System IL). In questo caso, l'impostazione di UIAccess non ha alcun effetto.

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a>Requisiti UIAccess per le applicazioni di Assistive Technology

Un'applicazione di Assistive Technology è un'applicazione desktop Windows Windows che interagisce con altri processi in esecuzione sul desktop e nella nuova interfaccia utente di Windows per ottenere informazioni dal sistema e dalle applicazioni. L'applicazione Assistive Technology può quindi fornire le informazioni agli utenti di accessibilità.

Un'applicazione Assistive Technology Ottiene l'accesso ad altri processi impostando il flag UIAccess nel manifesto dell'applicazione. Per usare il flag UIAccess, un'applicazione di Assistive Technology deve soddisfare i requisiti seguenti.

-   È necessario visualizzare, interagire o riflettere le informazioni di un'altra applicazione per fornire informazioni per uno scenario di accessibilità e/o
-   Richiedere l'esecuzione come finestra in primo piano per ottenere o visualizzare queste informazioni.

Per usare UIAccess, un'applicazione di Assistive Technology deve:

-   Essere firmato con un certificato per interagire con le applicazioni in esecuzione con un livello di privilegi più elevato.
-   Essere considerato attendibile dal sistema. L'applicazione deve essere installata in un percorso sicuro che richiede l'accesso a una richiesta di controllo dell'account utente (UAC). Ad esempio, la cartella Program Files.
-   Essere compilato con un file manifesto che include il flag uiAccess.

UIAccess non deve essere utilizzato:

-   Da applicazioni che non sono tecnologie per l'accesso facilitato.
-   Da applicazioni tecnologiche che consentono di visualizzare informazioni o interfaccia utente non rilevanti per lo scenario di accessibilità di destinazione.
-   Per le applicazioni che vogliono solo apparire sopra le altre applicazioni nella nuova interfaccia utente di Windows.
    > [!Note]  
    > Le applicazioni sviluppate per la nuova interfaccia utente di Windows non dispongono di UIAccess come opzione disponibile.

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a>Impostazione di UIAccess nel file manifesto dell'applicazione

Per accedere all'interfaccia utente del sistema protetto, le applicazioni devono essere compilate con un file manifesto che include un attributo speciale nel file manifesto. Questo attributo **uiAccess** è incluso nel tag **requestedExecutionLevel** , come illustrato nell'esempio di codice seguente.


```XML
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"> 
    <security> 
        <requestedPrivileges> 
        <requestedExecutionLevel 
            level="highestAvailable" 
            uiAccess="true" /> 
        </requestedPrivileges> 
    </security> 
</trustInfo> 
```



Il valore dell'attributo **Level** in questo codice è solo un esempio.

Per impostazione predefinita, **uiAccess** è "false". Se l'attributo viene omesso o se non è presente alcun manifesto, l'applicazione non può accedere all'interfaccia utente protetta.

Per ulteriori informazioni sulla sicurezza di Windows, sulla firma delle applicazioni e sulla creazione di manifesti, vedere [la storia degli sviluppatori di Windows Vista e Windows Server 2008: requisiti per lo sviluppo di applicazioni Windows Vista per il controllo dell'account utente](/previous-versions/aa905330(v=msdn.10)) in MSDN.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Nozioni fondamentali sull'automazione interfaccia utente](entry-uiautocore-overview.md)
</dt> </dl>

 

 