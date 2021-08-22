---
title: Considerazioni sulla sicurezza per assistive Technologies
description: Le tecnologie di assistive sono applicazioni eseguite sul desktop Windows e consentono agli utenti di accessibilità di interagire con il sistema operativo e altre applicazioni in esecuzione nel computer, incluse le applicazioni nella nuova interfaccia utente Windows.
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- Attributo uiAccess
- Automazione interfaccia utente,uiAccess
- attributo security,uiAccess
- Tag requestedExecutionLevel
- Automazione interfaccia utente,requestedExecutionLevel
- Automazione interfaccia utente,considerazioni sulla sicurezza
- Automazione interfaccia utente,file manifesto
- file manifesto
- controllo dell'account utente
- sicurezza, controllo dell'account utente
- sicurezza,file manifesto
- tag security,requestedExecutionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88ba97be98795be3725efaf76cf01297d7a00a2bb0112b0211581b3e0e4035f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563964"
---
# <a name="security-considerations-for-assistive-technologies"></a>Considerazioni sulla sicurezza per assistive Technologies

Le tecnologie di assistive sono applicazioni eseguite sul desktop Windows e consentono agli utenti di accessibilità di interagire con il sistema operativo e altre applicazioni in esecuzione nel computer, incluse le applicazioni nella nuova interfaccia utente Windows utente. Le applicazioni assistive technology funzionano recuperando le informazioni dal sistema operativo e da altre applicazioni e quindi presentando le informazioni in modo accessibile all'utente. Un'assistive technology può anche "guidare" a livello di codice il sistema operativo e altre applicazioni in base all'input dell'utente.

La natura delle assistive technology richiede che si esere oltre i limiti dei processi e che abbia accesso ai processi eseguiti a un livello di integrità superiore rispetto a se stessi. Un'assistive technology'applicazione viene eseguita a livello di servizio medio. Ad esempio, quando l'utente tenta di eseguire un'attività che richiede privilegi amministrativi, Windows una finestra di dialogo che richiede il consenso per continuare. Questa finestra di dialogo viene eseguita a un livello il più elevato per proteggerla dalla comunicazione tra processi, in modo che il software dannoso non possa simulare l'input dell'utente. Analogamente, la schermata di accesso al desktop viene eseguita con un livello di accesso superiore per impedire l'accesso da parte di altri processi.

Le applicazioni di assistive technology richiedono in genere l'accesso agli elementi dell'interfaccia utente del sistema protetti o ad altri processi che potrebbero essere in esecuzione a un livello di privilegi superiore. Pertanto, assistive technology applicazioni devono essere attendibili dal sistema e devono essere eseguite con privilegi speciali.

Per ottenere l'accesso a processi IL più elevati, un'applicazione assistive technology deve impostare il flag UIAccess nel manifesto dell'applicazione ed essere avviata da un utente con privilegi di amministratore.

> [!NOTE]
> I privilegi di accesso sono vincolati nel modo seguente:
>
> - Un'applicazione che non dispone di UIAccess nel manifesto inizia con un livello di accesso ili medio e non può accedere all'interfaccia utente del processo con privilegi elevati ("medium+").
> - Un'applicazione che ha UIAccess nel manifesto e viene avviata da un utente che non fa parte del gruppo administrators, avvia come "medium+" IL e non può accedere all'interfaccia utente con privilegi elevati (nessun elemento in esecuzione come "high" IL, ad esempio le app avviate tramite un clic con il pulsante destro del mouse **su -> Esegui come amministratore**).
> - Un'applicazione dispone dell'accesso all'interfaccia utente e viene avviata da un utente amministratore come "high" IL e può accedere all'interfaccia utente con privilegi elevati perché ha lo stesso il.
>
> UIAccess non è sufficiente perché un processo si sposti verso l'alto attraverso il limite IL.

Oltre ad avere accesso a processi IL più elevati, un'applicazione assistive technology con questi privilegi può essere eseguita come applicazione più in alto nell'ordine z in qualsiasi momento, il che significa che un'applicazione assistive technology può essere visibile e disponibile ogni volta che l'utente ne ha bisogno.

> [!Important]
> Nessuno degli scenari elencati in precedenza fornisce l'accesso all'interfaccia utente in esecuzione nel servizio il sistema. Ciò è possibile solo se il processo viene avviato nel desktop di controllo dell'account utente (UAC) in SYSTEM (e system IL). In questo caso, l'impostazione di UIAccess non ha alcun effetto.

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a>Requisiti di accesso all'interfaccia utente per le applicazioni assistive technology

Un'applicazione assistive technology è un'applicazione desktop Windows Windows che interagisce con altri processi in esecuzione sul desktop e nella nuova interfaccia utente di Windows per ottenere informazioni dal sistema e dalle applicazioni. L assistive technology appalto può quindi fornire le informazioni agli utenti dell'accessibilità.

Un assistive technology'applicazione ottiene l'accesso ad altri processi impostando il flag UIAccess nel manifesto dell'applicazione. Per usare il flag UIAccess, un'applicazione assistive technology deve soddisfare i requisiti seguenti.

-   Richiedere di visualizzare, interagire o riflettere le informazioni di un'altra applicazione per fornire informazioni per uno scenario di accessibilità e/o
-   Richiedere l'esecuzione come finestra più in alto per ottenere o visualizzare queste informazioni.

Per usare UIAccess, un'assistive technology deve:

-   Essere firmati con un certificato per interagire con le applicazioni in esecuzione a un livello di privilegi superiore.
-   Essere considerato attendibile dal sistema. L'applicazione deve essere installata in una posizione sicura che richiede un prompt di controllo dell'account utente per l'accesso. Ad esempio, la cartella Programmi.
-   Essere compilato con un file manifesto che include il flag uiAccess.

UIAccess non deve essere usato:

-   Da applicazioni che non sono tecnologie di assistive.
-   Per assistive technology applicazioni che visualizzano informazioni o interfaccia utente che non sono rilevanti per lo scenario di accessibilità di destinazione.
-   Dalle applicazioni che vogliono semplicemente essere visualizzate sopra altre applicazioni nella nuova interfaccia Windows interfaccia utente.
    > [!Note]  
    > Le applicazioni sviluppate per la nuova interfaccia Windows non hanno UIAccess come opzione disponibile.

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a>Impostazione di UIAccess nel file manifesto dell'applicazione

Per ottenere l'accesso all'interfaccia utente di sistema protetta, le applicazioni devono essere compilate con un file manifesto che include un attributo speciale nel file manifesto. Questo **attributo uiAccess** è incluso nel tag **requestedExecutionLevel,** come illustrato nell'esempio di codice seguente.


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



Il valore **dell'attributo level** in questo codice è solo un esempio.

**UIAccess** è "false" per impostazione predefinita. Se l'attributo viene omesso o se non è presente alcun manifesto, l'applicazione non può accedere all'interfaccia utente protetta.

Per altre informazioni sulla sicurezza Windows, sulla firma delle applicazioni e sulla creazione di manifesti, vedere The [Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC) (Storia](/previous-versions/aa905330(v=msdn.10)) per sviluppatori di Windows Vista e Windows Server 2008: requisiti di sviluppo delle applicazioni di Windows Vista per il controllo dell'account utente) su MSDN.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Nozioni fondamentali sull'automazione interfaccia utente](entry-uiautocore-overview.md)
</dt> </dl>

 

 