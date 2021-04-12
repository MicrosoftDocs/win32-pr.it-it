---
title: Aggiunta di un controllo Media Player Windows incorporato
description: Aggiunta di un controllo Media Player Windows incorporato
ms.assetid: e002bf2a-c51a-448a-80a0-a35d6f32e9c0
keywords:
- Playlist Windows Media Metafile, aggiunta di controlli Media Player Windows incorporati
- playlist, aggiunta di controlli Media Player Windows incorporati
- playlist di metafile, aggiunta di controlli Media Player Windows incorporati
- Playlist Windows Media Metafile, controlli Media Player Windows incorporati
- playlist, controlli Media Player incorporati di Windows
- playlist di metafile, controlli Media Player Windows incorporati
- Aggiunta di controlli Media Player Windows incorporati
- controlli Media Player incorporati di Windows
- Windows Media Player, aggiunta di controlli incorporati
- Windows Media Player, controlli incorporati
- HTMLView, aggiunta di controlli Media Player incorporati di Windows
- HTMLView, controlli Media Player incorporati di Windows
- HTMLView, modello a oggetti di Windows Media Player
- HTMLView, modello a oggetti del lettore
- Modello a oggetti di Windows Media Player, informazioni
- modello a oggetti, informazioni
- Oggetto Player
- Windows Media, modello a oggetti del lettore
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1dea3b11f59bff2edbcef99f1acda5fd0cfcff46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396387"
---
# <a name="adding-an-embedded-windows-media-player-control"></a>Aggiunta di un controllo Media Player Windows incorporato

Esistono due motivi per cui è consigliabile aggiungere un'istanza incorporata di Windows Media Player alla presentazione di HTMLView. Prima di tutto, se si desidera visualizzare il contenuto video, è necessario utilizzare il controllo ActiveX di Windows Media Player. In secondo luogo, se si desidera sfruttare le funzionalità del modello a oggetti di Windows Media Player dalla pagina Web di HTMLView, è necessario utilizzare un'istanza del controllo Player a tale scopo.

## <a name="using-the-player-control-to-display-video-in-htmlview-content"></a>Uso del controllo Player per visualizzare il video nel contenuto di HTMLView

In genere, Windows Media Player Visualizza i video usando il riquadro video e visualizzazione della funzionalità **Now Playing** . Poiché HTMLView usa quest'area per visualizzare la pagina Web, è necessario fornire un'area di visualizzazione video aggiuntiva se si vuole che il lettore riproduca video. Questa operazione è facile da eseguire tramite il controllo ActiveX di Windows Media Player.

Per usare il controllo Player per visualizzare video, incorporare il controllo nella pagina Web HTMLView usando il tag **Object** . Si tratta della stessa tecnica usata per incorporare il controllo Player in una pagina Web in cui si vuole visualizzare il video. Nell'esempio di codice seguente viene illustrata la sintassi di base per incorporare il controllo Player in Internet Explorer:


```XML
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">
</OBJECT>

```



Il parametro *autostart* garantisce che il contenuto venga riprodotto automaticamente ogni volta che viene specificato un nuovo URL. Il valore specificato per *uiMode* dipende dall'utente, ma in genere si vuole specificare "None" durante la creazione di contenuto per le presentazioni di htmlview. Quando si incorpora il controllo Media Player Windows per visualizzare i video in questo modo, l'utente può controllare la riproduzione usando i controlli del lettore in modalità completa, pertanto non è necessario fornire controlli di trasporto aggiuntivi nella pagina Web. È possibile utilizzare lo spazio che in genere si alloca per i controlli di trasporto per visualizzare più testo, elementi grafici o collegamenti ad altro contenuto.

Non specificare un parametro *URL* quando si incorpora il controllo Media Player Windows in una pagina Web progettata per la visualizzazione in una presentazione htmlview. Specificare invece i file multimediali digitali nel file con estensione asx che consente di aprire il contenuto.

Dato che l'area di visualizzazione video è disponibile nella pagina Web di HTMLView, è possibile decidere dove posizionare il video e la dimensione desiderata per l'area di visualizzazione. Ad esempio, è possibile contenere l'oggetto **Player** all'interno di un elemento HTML **div** , quindi specificare la posizione in cui il **div** deve collocare la visualizzazione video nella pagina Web. È possibile modificare le dimensioni della visualizzazione video specificando i valori per gli attributi Height e Width dell'elemento **Object** . È anche possibile specificare questi valori usando il codice di script.

## <a name="using-the-player-object-model"></a>Uso del modello a oggetti del lettore

Il modello a oggetti di Windows Media Player espone proprietà, metodi ed eventi che è possibile usare nelle pagine Web di HTMLView. Quando si incorpora il controllo ActiveX di Windows Media Player nella pagina Web di HTMLView, è possibile accedere automaticamente al modello a oggetti del lettore.

Se si incorpora il controllo Windows Media Player nella pagina Web di HTMLView, non usare il modello a oggetti del lettore per specificare il file multimediale digitale da riprodurre. Se, ad esempio, si usa codice script per specificare un valore per la proprietà **URL** del controllo incorporato, la pagina Web HtmlView verrà scaricata dalla funzionalità **Now Playing** durante la riproduzione del file multimediale digitale. Per evitare che ciò accada, aprire sempre i file con estensione asx che includono i parametri HTMLView quando è necessario usare lo script per aprire il contenuto multimediale digitale dalla pagina Web di HTMLView.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Visualizzazione di pagine Web in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. uiMode**](player-uimode.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Impostazioni. avvio automatico**](settings-autostart.md)
</dt> </dl>

 

 




