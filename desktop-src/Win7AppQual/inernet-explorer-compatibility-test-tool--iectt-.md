---
description: Internet Explorer Compatibility Test Tool (IECTT)
ms.assetid: 11169540-555A-48A9-A4CD-535D5765C005
title: Internet Explorer Compatibility Test Tool (IECTT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12209664dc5aca037b30d938f9c25c9a0e25d02d84019c1a3cb43056a3af06df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998941"
---
# <a name="internet-explorer-compatibility-test-tool-iectt"></a>Internet Explorer Compatibility Test Tool (IECTT)

Lo Internet Explorer Compatibility Test Tool (IECTT) è un componente di [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install). Questo strumento consente di diagnosticare i problemi nelle applicazioni Web visualizzando i problemi in tempo reale e caricando facoltativamente i risultati in un database ACT. I risultati includono informazioni dettagliate sui possibili problemi di compatibilità e collegamenti per altre informazioni su ogni problema di compatibilità. IECTT consente anche di escludere problemi e modificare gli attributi disponibili.

## <a name="to-open-iectt"></a>Per aprire IECTT

1.  Installare Microsoft [Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).
2.  Fare clic sul pulsante **Start**, scegliere **Programmi,** Microsoft Application Compatibility **Toolkit 5.6,** Strumenti per sviluppatori e **tester** e quindi fare clic su Internet Explorer Strumento test di **compatibilità**.

Le sezioni seguenti descrivono scenari IECTT comuni.

## <a name="view-issues-in-real-time"></a>Visualizzare i problemi in tempo reale

È possibile individuare e visualizzare i problemi basati sul Web in tempo reale, durante il test dei siti Web e delle applicazioni Web in Windows Internet Explorer 7 e Windows Internet Explorer 8. Dopo aver completato il test, è possibile visualizzare i risultati nella schermata **Dati** live di IECTT.

## <a name="upload-issues-to-your-act-database"></a>Upload Problemi relativi al database ACT

È possibile caricare i problemi basati sul Web nel database ACT, che elabora  le informazioni e consente di visualizzare i risultati nella schermata Analizza di Application Compatibility Manager.

## <a name="collect-your-compatibility-data"></a>Raccogliere i dati di compatibilità

È possibile raccogliere i dati di compatibilità relativi al sito Web e alle applicazioni Web usando lo strumento IECTT con Internet Explorer 7 o Internet Explorer 7.

**Per raccogliere i dati di compatibilità**

1.  Chiudere tutte le finestre Windows Internet Explorer attive.
2.  In IECTT, sulla barra degli strumenti dello **Internet Explorer Compatibility Test Tool,** fare clic su **Abilita**.
3.  Aprire una Internet Explorer 7 o Internet Explorer 8.

    Viene visualizzato un messaggio che indica che la registrazione di valutazione della compatibilità è attivata.

4.  Visitare i siti Web o le applicazioni Web necessari per l'uso da parte dell'organizzazione. Quando si visita ogni sito, lo strumento IECTT visualizza, in tempo reale, i potenziali problemi di compatibilità.
5.  Al **termine, Internet Explorer barra** degli strumenti dello strumento **di** test di compatibilità fare clic su Disabilita.

    Il processo di registrazione della compatibilità viene completato e arrestato.

## <a name="filter-your-issue-results"></a>Filtrare i risultati del problema

È possibile filtrare i risultati IECTT in base al nome dell'oggetto, al tipo di problema o a entrambi.

**Per filtrare i risultati del problema**

1.  Nella schermata **dello Internet Explorer di test di compatibilità** fare clic su **Filtro**.

    Verrà **visualizzata la finestra di** dialogo Filtro problemi.

2.  Immettere il nome dell'oggetto che si intende visualizzare nella casella Immettere il **nome dell'oggetto** per cui visualizzare i problemi.

Per altre informazioni su questo strumento e altri strumenti per sviluppatori, vedere Che cos'è lo strumento di test di compatibilità [di Internet Explorer?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) in MSDN Library e il post di blog Registrazione compatibilità applicazioni [in IE8.](/archive/blogs/ie/application-compatibility-logging-in-ie8)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti per il debug di applicazioni Web e componenti aggiuntivi](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 
