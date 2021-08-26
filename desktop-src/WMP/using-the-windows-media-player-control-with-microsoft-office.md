---
title: Uso del controllo Windows Media Player con Microsoft Office
description: Uso del controllo Windows Media Player con Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Windows Media Player,incorporamento ActiveX controllo
- Windows Media Player a oggetti, incorporamento ActiveX controllo
- modello a oggetti, incorporamento ActiveX controllo
- Windows Media Player Mobile, incorporamento ActiveX controllo
- Windows Media Player ActiveX, incorporamento
- Windows Media Player Controllo ActiveX per dispositivi mobili, incorporamento
- ActiveX, incorporamento
- Windows Media Player,Office
- Windows Media Player a oggetti, Office
- modello a oggetti, Office
- Windows Media Player Mobile, Office
- Windows Media Player ActiveX controllo, Office
- Windows Media Player Controllo ActiveX mobile, Office
- ActiveX controllo, Office
- Office incorporamento di documenti
- incorporamento, Office documenti
- Windows Media Player ActiveX controllo, Excel
- Windows Media Player Controllo ActiveX per dispositivi mobili, Excel
- ActiveX controllo, Excel
- incorporamento, Excel fogli di calcolo
- Excel incorporamento del foglio di calcolo
- Windows Media Player ActiveX controllo, PowerPoint
- Windows Media Player Controllo ActiveX per dispositivi mobili, PowerPoint
- ActiveX controllo, PowerPoint
- incorporamento, PowerPoint presentazioni
- PowerPoint incorporamento della presentazione
- Windows Media Player ActiveX controllo, Word
- Windows Media Player Controllo ActiveX per dispositivi mobili,Word
- ActiveX controllo, Word
- Incorporamento di documenti di Word
- incorporamento, documenti di Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418c082cad2793e3ebd676c4d648339f9e637f46c7519efc1b426a44b69ee05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001401"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a>Uso del controllo Windows Media Player con Microsoft Office

Questa sezione descrive come incorporare il controllo Windows Media Player serie 9 o successive ActiveX in vari documenti creati usando Microsoft Office XP.

In Microsoft Word, Excel e PowerPoint®, incorporare il controllo selezionando Oggetto  dal **menu** **Inserisci,** quindi scegliendo Windows Media Player dall'elenco dei tipi di oggetto disponibili. Il Windows Media Player controllo viene visualizzato nel documento nella posizione corrente. È quindi possibile selezionare **Format Control** **(Format Object** in Excel) dal menu di scelta rapida per il controllo per modificare il layout, lo stile di ritorno a capo del testo e altre opzioni di formato. Per eseguire questa Excel, in Word e in Excel è necessario essere in modalità progettazione.

Dopo aver posizionato e formattato il controllo, è  possibile configurarlo usando la  finestra di dialogo Proprietà , accessibile dalla Casella degli strumenti di controllo o dal menu di scelta rapida in modalità progettazione per Word e Excel. Qui è possibile specificare le proprietà di base del controllo Player, ad esempio il nome del controllo, l'URL di un file multimediale digitale e la modalità dell'interfaccia utente. L'impostazione della proprietà **uiMode** su "none" nasconde tutti gli elementi del controllo, ad eccezione del video o della finestra di visualizzazione, consentendo di aggiungere pulsanti personalizzati e scrivere codice di script usando Visual Basic, Applications Edition (VBA) per gestire i clic sui pulsanti e gli eventi del controllo Player.

Nella finestra  di dialogo Proprietà di base è anche possibile accedere alla finestra di dialogo Proprietà controllo **Windows Media Player** più sofisticata facendo doppio clic sulla riga "(Personalizzata)" o facendo clic sui puntini di sospensione ("...") dopo aver selezionato la riga. Da questa finestra di dialogo è possibile modificare tutte le proprietà del controllo Player disponibili.

> [!Note]  
> È necessario prestare attenzione a non eseguire azioni nei gestori eventi del controllo Player che comportano l'eliminazione del controllo. Ad esempio, se si incorpora il controllo Windows Media Player in una diapositiva in una presentazione PowerPoint, non chiamare il metodo PowerPoint **Next** dall'evento **Player openStateChange** o da qualsiasi altro evento.

 

> [!Note]  
> Inoltre, non è necessario impostare la proprietà **Player.URL** da un gestore dell'evento del controllo Player.

 

In FrontPage aggiungere il controllo Windows Media Player a una pagina Web selezionando **Componente Web** **dal** menu Inserisci. Nella finestra di **dialogo Inserisci componente** Web  selezionare **Controlli** avanzati dall'elenco Tipo di componente, quindi selezionare ActiveX **controllo dall'elenco** di opzioni di controllo. Nella finestra successiva della finestra di dialogo selezionare **Windows Media Player**. Se non è elencato, **fare** clic su Personalizza e selezionare la **Windows Media Player** di controllo nell'elenco **Controllo.**

Dopo aver incorporato Windows Media Player controllo, è possibile posizionarlo e ridimensionarlo e modificarne le proprietà selezionando ActiveX **Proprietà** controllo dal menu di scelta rapida per il controllo. Nella visualizzazione HTML i valori delle proprietà specificati vengono visualizzati nell'elemento OBJECT che rappresenta il Windows Media Player controllo. Il nome dell'oggetto viene visualizzato come attributo ID e le proprietà del controllo vengono visualizzate come tag PARAM. Il nome dell'oggetto consente di accedere al modello Windows Media Player a oggetti di controllo, che è possibile programmare usando Microsoft JScript. Per altre informazioni, vedere [Uso del controllo Windows Media Player in una pagina Web](using-the-windows-media-player-control-in-a-web-page.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida al controllo del giocatore**](player-control-guide.md)
</dt> </dl>

 

 




