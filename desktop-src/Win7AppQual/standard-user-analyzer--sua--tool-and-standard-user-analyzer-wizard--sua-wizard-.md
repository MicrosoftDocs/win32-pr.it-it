---
description: Informazioni su come usare lo strumento Standard User Analyzer (SUA) e la procedura guidata di SUA per testare le applicazioni e rilevare potenziali problemi di compatibilità.
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: Strumento Analizzatore utente standard e procedura guidata Analizzatore utente standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a897c603f185db775c059e4b3dd4a040cba9ad
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314584"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a>Strumento Analizzatore utente standard e procedura guidata Analizzatore utente standard

## <a name="affected-platforms"></a>Piattaforme interessate

**Client:** Windows XP, Windows Vista, Windows 7  
**Server:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  

## <a name="description"></a>Descrizione

Application Compatibility Toolkit include lo strumento Standard User Analyzer (SUA) e la procedura guidata dell'Analizzatore utente standard. Questi strumenti consentono di testare le applicazioni e di monitorare le chiamate API per rilevare potenziali problemi di compatibilità dovuti alla funzionalità controllo dell'account utente (UAC) nel sistema operativo Windows 7.

UAC, noto in precedenza come account utente limitato (LUA), richiede che tutti gli utenti (inclusi i membri del gruppo Administrator) vengano eseguiti come utenti standard utilizzando la finestra di dialogo richiesta di sicurezza finché l'applicazione non viene deliberatamente elevata. Tuttavia, le applicazioni che richiedono l'accesso e i privilegi per percorsi non disponibili per un utente standard non possono essere eseguite correttamente con il ruolo utente standard.

## <a name="usage"></a>Utilizzo

Nelle sezioni seguenti vengono fornite informazioni dettagliate sull'utilizzo degli strumenti della procedura guidata di SUA e di SUA.

**Strumento SUA**

Lo strumento SUA consente di analizzare un'applicazione, esaminare un report dettagliato sui problemi correlati al controllo dell'account utente e quindi applicare le attenuazioni delle applicazioni suggerite e selezionate, come illustrato nel diagramma di flusso seguente.

![Diagramma che mostra il flusso dello strumento S U A.](images/act-suaflowchart-appcookbook.gif)

*Strumento e virtualizzazione di SUA*

Solo lo strumento SUA consente di attivare e disattivare la funzionalità di virtualizzazione. Con la disattivazione della funzionalità di virtualizzazione, l'applicazione testata si comporterà in modo più simile quando funziona nel sistema operativo Windows XP.

*Strumento SUA e privilegi elevati*

Solo lo strumento SUA consente di attivare e disattivare la funzionalità di **avvio con privilegi elevati** . La funzionalità di avvio con privilegi elevati consente di eseguire l'applicazione selezionata come amministratore o come utente standard. A seconda della selezione effettuata, si troveranno tipi diversi di problemi correlati a UAC. Se si deseleziona la casella di controllo avvia con privilegi **elevati** , l'applicazione viene eseguita con privilegi di amministratore completi, consentendo a sua di prevedere i problemi che potrebbero verificarsi per un utente standard. Se si seleziona la casella di controllo avvia con privilegi elevati, vengono visualizzati gli errori che risultano dall'applicazione in esecuzione e generano errori.

**Procedura guidata di SUA**

La procedura guidata di SUA guida consente di seguire un processo dettagliato che consente di analizzare un'applicazione e quindi di applicare le attenuazioni delle applicazioni suggerite e selezionate, come illustrato nel diagramma di flusso seguente. A differenza dello strumento SUA, la procedura guidata non consente di esaminare i problemi dettagliati relativi all'UAC.

![Diagramma che mostra il flusso della procedura guidata S U A.](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Download di Application Compatibility Toolkit](/windows-hardware/get-started/adk-install)
-   [Informazioni sugli strumenti dell'Analizzatore utente standard](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))
-   [Riferimento tecnico per l'Analizzatore utente standard](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))
-   [Test e attenuazione dei problemi tramite gli strumenti di sviluppo](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))
-   [Compatibilità delle applicazioni e controllo dell'account utente](/previous-versions/windows/)

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.

 

 

 
