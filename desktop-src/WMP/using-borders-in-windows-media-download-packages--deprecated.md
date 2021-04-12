---
title: Uso dei bordi nei pacchetti di download di Windows Media (deprecato)
description: Uso dei bordi nei pacchetti di download di Windows Media (deprecato)
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Metafile di Windows Media, pacchetti di download di Windows Media
- Windows Media Player, pacchetti di download di Windows Media
- Metafile, pacchetti di download di Windows Media
- Windows Media, pacchetti di download di Windows Media
- bordi, informazioni
- Pacchetti di download di Windows Media, bordi
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 87f7d0fec341bb79bfe9b8dd739b63a9ba3a66ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396162"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a>Uso dei bordi nei pacchetti di download di Windows Media (deprecato)

Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.

I bordi consentono di creare un'interfaccia utente grafica personalizzata per il contenuto in pacchetto. Il bordo può includere elementi quali immagini, controlli interattivi e collegamenti a siti Web. È possibile usare i bordi nei casi in cui si vuole aggiungere altro valore al contenuto incluso nel pacchetto, ad esempio per la personalizzazione o la pubblicità. Dopo che gli utenti hanno scaricato e aperto il pacchetto di download di Windows Media, Windows Media Player visualizza automaticamente il bordo personalizzato quando riproduce il contenuto in pacchetto.

Diversamente da un'interfaccia personalizzata, che consente agli utenti di sostituire completamente l'interfaccia utente di Windows Media Player, viene visualizzato un bordo solo nel riquadro **ora di riproduzione** del lettore in modalità piena. Tuttavia, per creare i bordi vengono usati anche gli stessi strumenti e tecnologie usati per creare le interfacce. Nella figura seguente viene illustrato un bordo.

![bordo visualizzato in Windows Media Player 10](images/border-v10.png)

È importante comprendere le tecniche di base per la creazione di un'interfaccia prima di provare a creare un bordo. La programmazione di bordi viene eseguita utilizzando due linguaggi di programmazione: Extensible Markup Language (XML) e Microsoft JScript. XML viene utilizzato per definire elementi di interfaccia quali pulsanti, dispositivi di scorrimento e caselle di testo. Non è necessario comprendere tutti i dettagli di XML poiché non è necessario scrivere nuovi elementi di codice XML. è possibile utilizzare semplicemente quelli forniti da Windows Media Player. Sebbene non sia necessario per la creazione di bordi, JScript può essere utilizzato per fornire funzionalità aggiuntive.

Un file di bordo compresso con estensione WMZ include un file di definizione del bordo con estensione del nome di file WMS e tutti i file di immagine utilizzati all'interno del bordo.

Per includere un bordo in un pacchetto di download di Windows Media, è sufficiente creare un bordo e fare riferimento a tale bordo in una playlist Windows Media Metafile. Il file di bordo viene caricato in Windows Media Player dopo che il lettore analizza il metafile e interpreta l'elemento **Skin** che fa riferimento al bordo. L'elemento **Skin** viene usato solo per i bordi e l'attributo href dell'elemento **Skin** può fare riferimento a una sola interfaccia per ogni pacchetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Bordi per Windows Media Player (deprecato)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Pacchetti di download di Windows Media (deprecato)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Interfacce di Media Player Windows**](windows-media-player-skins.md)
</dt> </dl>

 

 




