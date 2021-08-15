---
title: Uso di bordi in Windows pacchetti di download multimediali (deprecato)
description: Uso di bordi in Windows pacchetti di download multimediali (deprecato)
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Windows Metafile multimediali,Windows pacchetti di download multimediali
- Windows Media Player,Windows pacchetti di download multimediali
- metafile, Windows di download multimediale
- Windows Pacchetti di Windows multimediali
- bordi, informazioni
- Windows Pacchetti di download multimediale, bordi
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 851edf0d2291d41212cf44829219235426463733ce95a99c3d59187eba490ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117931810"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a>Uso di bordi in Windows pacchetti di download multimediali (deprecato)

Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.

I bordi consentono di creare un'interfaccia utente grafica personalizzata per il contenuto in pacchetto. Il bordo può includere elementi quali immagini, controlli interattivi e collegamenti a siti Web. È possibile usare i bordi nei casi in cui si vuole aggiungere ulteriore valore al contenuto in pacchetto, ad esempio per la personalizzazione o la pubblicità. Dopo che gli utenti hanno scaricato e aperto il pacchetto Windows Media Download, Windows Media Player automaticamente il bordo personalizzato quando riproduce il contenuto in pacchetto.

A differenza di un'interfaccia, che consente agli utenti di sostituire completamente l'interfaccia utente Windows Media Player, un bordo viene visualizzato solo nel riquadro In riproduzione del lettore in modalità completa.  Tuttavia, per creare bordi vengono usati anche gli stessi strumenti e tecnologie usati per creare le skin. La figura seguente mostra un bordo.

![bordo visualizzato in Windows Media Player 10](images/border-v10.png)

È importante comprendere le tecniche di base per la creazione di un'interfaccia prima di tentare di creare un bordo. La programmazione dei bordi viene eseguita usando due linguaggi di programmazione: Extensible Markup Language (XML) e Microsoft JScript. XML viene usato per definire gli elementi dell'interfaccia, ad esempio pulsanti, dispositivi di scorrimento e caselle di testo. Non è necessario comprendere tutti i dettagli di XML poiché non è necessario scrivere nuovi elementi di codice XML. è possibile usare semplicemente quelli forniti da Windows Media Player. Sebbene JScript non sia necessario per la creazione di bordi, può essere usato per fornire funzionalità aggiuntive.

Un file di bordo compresso con estensione wmz include un file di definizione del bordo con estensione wms e tutti i file di immagine usati all'interno del bordo.

Per includere un bordo in un pacchetto Windows Media Download, è sufficiente creare un bordo e fare riferimento a tale bordo in una playlist Windows metafile multimediale. Il file del bordo viene caricato Windows Media Player lettore analizza il metafile e interpreta **l'elemento SKIN** che fa riferimento al bordo. **L'elemento SKIN** viene usato solo per i bordi e l'attributo HREF dell'elemento **SKIN** può fare riferimento a una sola interfaccia per ogni pacchetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Bordi per Windows Media Player (deprecato)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Windows Pacchetti di download multimediali (deprecati)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Windows Media Player Pelli**](windows-media-player-skins.md)
</dt> </dl>

 

 




