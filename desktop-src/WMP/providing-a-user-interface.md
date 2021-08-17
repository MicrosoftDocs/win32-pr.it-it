---
title: Fornire un Interfaccia utente
description: Fornire un Interfaccia utente
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Windows Media Player plug-in, pagine delle proprietà
- plug-in, pagine delle proprietà
- plug-in di elaborazione del segnale digitale, pagine delle proprietà
- plug-in DSP, pagine delle proprietà
- plug-in di elaborazione del segnale digitale, interfaccia utente
- Plug-in DSP, interfaccia utente
- pagine delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb80525fa4b32845608eebb32752871a038aa6e01088baeebce5bc5f8c84b4bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746739"
---
# <a name="providing-a-user-interface"></a>Fornire un Interfaccia utente

I plug-in DSP possono fornire una pagina delle proprietà per creare un'interfaccia utente. A tale scopo, il plug-in deve includere un oggetto pagina delle proprietà che fornisce un'implementazione di **un'interfaccia IPropertyPage.** L'oggetto plug-in DSP deve implementare **ISpecifyPropertyPages::GetPages**, che consente a Windows Media Player di individuare e identificare la pagina delle proprietà corretta per il plug-in.

**Visualizzazione di un'immagine di stato**

I plug-in DSP possono visualizzare una piccola grafica, o una serie di grafica, nell'area di stato Windows Media Player per notificare all'utente che un plug-in è attivo. Per supportare questa funzionalità, il plug-in deve implementare **l'interfaccia IPropertyBag.** Windows Media Player chiama **IPropertyBag::Read**, fornendo un puntatore al nome di proprietà richiesto "IconStreams", che fa distinzione tra maiuscole e minuscole, e un puntatore a una struttura **VARIANT** che riceve i dati per l'immagine. Il plug-in crea un oggetto **IStream** (o UN SAFEARRAY di oggetti **IStream** se sono presenti più elementi grafici), carica i dati grafici, incluse le informazioni di intestazione, nel flusso e quindi restituisce un puntatore all'oggetto **IStream** usando il membro **punkVal** della struttura **VARIANT.** Se il plug-in fornisce un solo elemento grafico, specifica il membro **vt** della struttura **VARIANT** come VT \_ UNKNOWN. Se il plug-in fornisce più oggetti **IStream** grafici usando un safearray, specifica il membro **vt** della struttura **VARIANT** come VT \_ ARRAY.

La grafica può essere archiviata in diversi formati di file, tra cui:

**BMP**

Microsoft Windows bitmap non sono compresse.

**JPEG**

Formato di immagine compressa comunemente usato per le pagine Web. I file in formato JPEG in genere .jpg estensioni di file.

**GIF**

Formato di immagine compressa comunemente usato per le pagine Web.

**PNG**

Formato di immagine compressa comunemente usato per le pagine Web.

Le dimensioni massime per la grafica plug-in DSP sono 38 pixel di larghezza e 14 pixel di altezza.

Il flusso di byte **IStream** contenente l'immagine di stato deve includere informazioni sull'intestazione. Senza informazioni sull'intestazione, Windows Media Player non è in grado di identificare correttamente il tipo di immagine e pertanto non carica l'immagine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica degli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




