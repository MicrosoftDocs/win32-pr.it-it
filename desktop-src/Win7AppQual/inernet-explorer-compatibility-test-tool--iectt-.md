---
description: .
ms.assetid: 11169540-555A-48A9-A4CD-535D5765C005
title: Internet Explorer Compatibility Test Tool (IECTT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25e39263f448c7e11db1be32463b3801e4a8761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313699"
---
# <a name="internet-explorer-compatibility-test-tool-iectt"></a>Internet Explorer Compatibility Test Tool (IECTT)

Lo strumento di verifica della compatibilità di Internet Explorer (IECTT) è un componente di [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install). Questo strumento consente di diagnosticare i problemi nelle applicazioni Web visualizzando i problemi in tempo reale e, facoltativamente, di caricare i risultati in un database ACT. I risultati includono informazioni dettagliate sui possibili problemi di compatibilità e sui collegamenti per ulteriori informazioni su ogni problema di compatibilità. IECTT consente inoltre di escludere i problemi e modificare gli attributi disponibili.

## <a name="to-open-iectt"></a>Per aprire IECTT

1.  Installare [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).
2.  Fare clic sul pulsante **Start**, scegliere **programmi**, **Microsoft Application Compatibility Toolkit 5,6**, scegliere **strumenti per sviluppatori e tester**, quindi fare clic su **strumento di test di compatibilità di Internet Explorer**.

Le sezioni seguenti descrivono scenari IECTT comuni.

## <a name="view-issues-in-real-time"></a>Visualizza i problemi in tempo reale

È possibile individuare e visualizzare i problemi basati sul Web in tempo reale, mentre si esegue il test di siti Web e applicazioni Web in Windows Internet Explorer 7 e Windows Internet Explorer 8. Dopo aver completato il test, è possibile visualizzare i risultati nella schermata **Live Data** del IECTT.

## <a name="upload-issues-to-your-act-database"></a>Caricare problemi nel database ACT

È possibile caricare i problemi basati sul Web nel database ACT, che elabora le informazioni e consente di visualizzare i risultati nella schermata **analizza** di gestione compatibilità applicazioni.

## <a name="collect-your-compatibility-data"></a>Raccogliere i dati di compatibilità

È possibile raccogliere i dati di compatibilità del sito Web e dell'applicazione Web utilizzando lo strumento IECTT con Internet Explorer 7 o Internet Explorer 7.

**Per raccogliere i dati di compatibilità**

1.  Chiudere tutte le finestre di Windows Internet Explorer attive.
2.  In IECTT, sulla barra degli strumenti di **test di compatibilità di Internet Explorer** , fare clic su **Abilita**.
3.  Aprire una finestra di Internet Explorer 7 o Internet Explorer 8.

    Viene visualizzato un messaggio che indica che la registrazione della valutazione della compatibilità è attivata.

4.  Visitare i siti Web o le applicazioni Web che sono necessari per l'uso da parte dell'organizzazione. Quando si visita ogni sito, lo strumento IECTT Visualizza in tempo reale i potenziali problemi di compatibilità.
5.  Sulla barra degli strumenti di **test di compatibilità di Internet Explorer** fare clic su **Disabilita** al termine dell'operazione.

    Il processo di registrazione della compatibilità termina e si arresta.

## <a name="filter-your-issue-results"></a>Filtrare i risultati del problema

È possibile filtrare i risultati di IECTT in base al nome dell'oggetto, al tipo di problema o a entrambi.

**Per filtrare i risultati del problema**

1.  Nella schermata dello **strumento di test della compatibilità di Internet Explorer** fare clic su **filtro**.

    Verrà visualizzata la finestra di dialogo **filtro problemi** .

2.  Immettere il nome dell'oggetto che si desidera visualizzare nella casella **immettere il nome dell'oggetto per visualizzare i problemi relativi** a.

Per ulteriori informazioni su questo strumento e sugli altri strumenti per sviluppatori, vedere la pagina relativa [allo strumento di test della compatibilità di Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) in MSDN Library e il post di Blog relativo alla [registrazione per la compatibilità delle applicazioni in IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti per il debug di applicazioni Web e componenti aggiuntivi](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 
