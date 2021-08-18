---
description: Informazioni su come usare lo strumento Analizzatore utenti Standard (SUA) e la procedura guidata SUA per testare le applicazioni e rilevare potenziali problemi di compatibilità.
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: Strumento Analizzatore utente standard e procedura guidata Analizzatore utente standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fa9329f2f42dd8fc3b948388ef44948deca052a919ca50704cbccedc83fca84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994676"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a>Strumento Analizzatore utente standard e procedura guidata Analizzatore utente standard

## <a name="affected-platforms"></a>Piattaforme interessate

**Client:** Windows XP, Windows Vista, Windows 7  
**Server:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  

## <a name="description"></a>Descrizione

L'Toolkit compatibilità delle applicazioni include lo strumento Analizzatore utenti standard (SUA) e la Procedura guidata Analizzatore utenti standard .NET. Questi strumenti consentono di testare le applicazioni e di monitorare le chiamate API per rilevare potenziali problemi di compatibilità dovuti alla funzionalità Controllo dell'account utente nel sistema operativo Windows 7.

Il controllo dell'account utente, noto in precedenza come Account utente limitato (LUA), richiede che tutti gli utenti (inclusi i membri del gruppo Amministratore) eseguano come utenti Standard usando la finestra di dialogo della richiesta di sicurezza fino a quando l'applicazione non viene deliberatamente elevata. Tuttavia, le applicazioni che richiedono l'accesso e i privilegi per le posizioni non disponibili per un utente Standard non possono essere eseguite correttamente con il ruolo Utente standard.

## <a name="usage"></a>Utilizzo

Le sezioni seguenti forniscono informazioni dettagliate sull'uso degli strumenti della procedura guidata SUA e SUA.

**Strumento SUA**

Lo strumento SUA consente di analizzare un'applicazione, esaminare un report dettagliato sui problemi correlati al controllo dell'account utente e quindi applicare le mitigazioni dell'applicazione suggerite e selezionate, come illustrato nel diagramma di flusso seguente.

![Diagramma che mostra il flusso dello strumento S U A.](images/act-suaflowchart-appcookbook.gif)

*Strumento SUA e virtualizzazione*

Solo lo strumento SUA consente di attivare e disattivare la funzionalità di virtualizzazione. Disattivando la funzionalità di virtualizzazione, l'applicazione testata si comporterà più come quando funziona nel Windows sistema operativo XP.

*Strumento SUA e privilegi elevati*

Solo lo strumento SUA consente di attivare e disattivare la **funzionalità Avvia con privilegi** elevati. La funzionalità Avvia con privilegi elevati consente all'applicazione selezionata di essere eseguita come amministratore o come utente standard. A seconda della selezione, si individuano diversi tipi di problemi correlati al controllo dell'account utente. Se si deseleziona la **casella di** controllo Avvia con privilegi elevati, l'applicazione verrà eseguita con privilegi di amministratore completi, che consente a SUA di stimare i problemi che potrebbero verificarsi per un utente standard. Se si seleziona la casella di controllo Avvia con privilegi elevati, verranno visualizzati gli errori risultanti dall'applicazione effettivamente in esecuzione e che generano errori.

**Procedura guidata SUA**

La procedura guidata SUA consente di seguire un processo guidato, passo dopo passo, in base al quale è possibile analizzare un'applicazione e quindi applicare le mitigazioni dell'applicazione suggerite e selezionate, come illustrato nel diagramma di flusso seguente. A differenza dello strumento SUA, la procedura guidata non consente una revisione dei problemi dettagliati relativi al controllo dell'account utente.

![Diagramma che mostra il flusso della procedura guidata S U A.](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Compatibilità delle applicazioni Toolkit download](/windows-hardware/get-started/adk-install)
-   [Informazioni sugli strumenti dell'analizzatore utenti standard](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))
-   [Informazioni di riferimento tecniche su Analizzatore utenti standard](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))
-   [Test e mitigazione dei problemi tramite gli strumenti di sviluppo](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))
-   [Compatibilità delle applicazioni e controllo dell'account utente](/previous-versions/windows/)

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.

 

 

 
