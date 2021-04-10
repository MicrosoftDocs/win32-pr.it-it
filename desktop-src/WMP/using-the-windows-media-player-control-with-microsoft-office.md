---
title: Uso del controllo Media Player di Windows con Microsoft Office
description: Uso del controllo Media Player di Windows con Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Windows Media Player, Office
- Modello a oggetti di Windows Media Player, Office
- modello a oggetti, Office
- Windows Media Player Mobile, Office
- Windows Media Player ActiveX Control, Office
- Controllo ActiveX Windows Media Player Mobile, Office
- Controllo ActiveX, Office
- Incorporamento di documenti di Office
- incorporamento, documenti di Office
- Controllo ActiveX di Windows Media Player, Excel
- Controllo ActiveX Windows Media Player Mobile, Excel
- Controllo ActiveX, Excel
- incorporamento, fogli di calcolo di Excel
- Incorporamento del foglio di calcolo di Excel
- Controllo ActiveX di Windows Media Player, PowerPoint
- Controllo ActiveX Windows Media Player Mobile, PowerPoint
- Controllo ActiveX, PowerPoint
- incorporamento, presentazioni di PowerPoint
- Presentazione dell'incorporamento in PowerPoint
- Controllo ActiveX di Windows Media Player, Word
- Controllo ActiveX Windows Media Player Mobile, Word
- Controllo ActiveX, Word
- Incorporamento di documenti di Word
- incorporamento, documenti di Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504b46b4fb409dede108c41b43014c3aaeae5ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955530"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a>Uso del controllo Media Player di Windows con Microsoft Office

In questa sezione viene descritto come incorporare il controllo ActiveX Windows Media Player 9 o versioni successive in diversi documenti creati con Microsoft Office XP.

In Microsoft Word, Excel e PowerPoint® è possibile incorporare il controllo selezionando **oggetto** dal menu **Inserisci** , quindi scegliendo **Windows Media Player** dall'elenco dei tipi di oggetto disponibili. Il controllo Media Player Windows viene visualizzato nel documento nella posizione corrente. È quindi possibile selezionare **formato controllo** ( **Formatta oggetto** in Excel) dal menu di scelta rapida per il controllo per modificare il layout, lo stile di ritorno a capo del testo e altre opzioni di formattazione. Per eseguire questa operazione in Word ed Excel, è necessario essere in modalità progettazione.

Dopo aver posizionato e formattato il controllo, è possibile configurarlo utilizzando la finestra di dialogo **Proprietà** , accessibile dalla **casella degli strumenti controllo** o dal menu di scelta rapida in modalità progettazione per Word ed Excel. Qui è possibile specificare le proprietà di base del controllo Player, ad esempio il nome del controllo, l'URL di un file multimediale digitale e la modalità dell'interfaccia utente. Se si imposta la proprietà **uiMode** su "None", tutti gli elementi del controllo vengono nascosti, ad eccezione della finestra video o visualizzazione, consentendo di aggiungere pulsanti personalizzati e scrivere codice script usando Visual Basic, Applications Edition (VBA) per gestire i clic del pulsante e gli eventi di controllo del lettore.

Nella finestra di dialogo **Proprietà** di base è inoltre possibile accedere alla finestra di dialogo **proprietà del controllo di Windows Media Player** più sofisticate facendo doppio clic sulla riga "(personalizzata)" oppure facendo clic sul pulsante con i puntini di sospensione ("...") dopo aver selezionato la riga. Da questa finestra di dialogo è possibile modificare tutte le proprietà del controllo lettore disponibili.

> [!Note]  
> È necessario prestare attenzione a non eseguire azioni nei gestori di eventi di controllo del lettore che comporteranno la distruzione del controllo. Se ad esempio si incorpora il controllo Windows Media Player in una diapositiva in una presentazione di PowerPoint, non chiamare il metodo **Next** di PowerPoint dall'evento Player **openStateChange** o da qualsiasi altro evento.

 

> [!Note]  
> Inoltre, è consigliabile non impostare la proprietà **Player. URL** da un gestore eventi di controllo del lettore.

 

In FrontPage aggiungere il controllo Media Player Windows a una pagina Web selezionando **componente Web** dal menu **Inserisci** . Nella finestra di dialogo **Inserisci componente Web** selezionare **controlli avanzati** nell'elenco **tipo componente** , quindi selezionare **controllo ActiveX** nell'elenco delle opzioni di controllo. Nella finestra successiva della finestra di dialogo selezionare **Windows Media Player**. Se non è elencato, fare clic su **Personalizza** e selezionare la casella di controllo **Windows Media Player** nell'elenco di **controllo** .

Dopo aver incorporato il controllo Media Player di Windows, è possibile posizionarlo e ridimensionarlo e modificarne le proprietà selezionando **proprietà del controllo ActiveX** dal menu di scelta rapida per il controllo. Nella visualizzazione HTML, i valori delle proprietà specificati vengono visualizzati nell'elemento oggetto che rappresenta il controllo Media Player di Windows. Il nome dell'oggetto viene visualizzato come attributo ID e le proprietà del controllo vengono visualizzate come tag PARAM. Il nome dell'oggetto consente di accedere al modello a oggetti di controllo Media Player di Windows, che è possibile programmare utilizzando Microsoft JScript. Per ulteriori informazioni, vedere [utilizzo del controllo Windows Media Player in una pagina Web](using-the-windows-media-player-control-in-a-web-page.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida al controllo del lettore**](player-control-guide.md)
</dt> </dl>

 

 




