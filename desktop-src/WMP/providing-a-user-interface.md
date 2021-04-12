---
title: Fornire un'interfaccia utente
description: Fornire un'interfaccia utente
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Plug-in di Windows Media Player, pagine delle proprietà
- plug-in, pagine delle proprietà
- plug-in di elaborazione dei segnali digitali, pagine delle proprietà
- Plug-in DSP, pagine delle proprietà
- plug-in per l'elaborazione di segnali digitali, interfaccia utente
- Plug-in DSP, interfaccia utente
- pagine delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d708d1256faf7096d15a7596a9635a33173d22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221838"
---
# <a name="providing-a-user-interface"></a>Fornire un'interfaccia utente

I plug-in DSP possono fornire una pagina delle proprietà per creare un'interfaccia utente. A tale scopo, il plug-in deve includere un oggetto pagina delle proprietà che fornisce un'implementazione di un'interfaccia **IPropertyPage** . L'oggetto plug-in DSP deve implementare **ISpecifyPropertyPages:: GetPages**, che consente a Windows Media Player di individuare e identificare la pagina delle proprietà corretta per il plug-in.

**Visualizzazione di un'immagine di stato**

I plug-in DSP possono visualizzare un piccolo grafico o una serie di elementi grafici nell'area stato Media Player Windows per notificare all'utente che è attivo un plug-in. Per supportare questa funzionalità, il plug-in deve implementare l'interfaccia **IPropertyBag** . Windows Media Player chiama **IPropertyBag:: Read**, fornendo un puntatore al nome di proprietà richiesto "IconStreams", che fa distinzione tra maiuscole e minuscole, e un puntatore a una struttura **Variant** che riceve i dati per l'elemento grafico. Il plug-in crea un oggetto **IStream** (o un SAFEARRAY di oggetti **IStream** se sono presenti più elementi grafici), quindi carica i dati grafici, incluse le informazioni di intestazione, nel flusso, quindi restituisce un puntatore all'oggetto **IStream** usando il membro **punkVal** della struttura **Variant** . Se il plug-in fornisce un solo elemento grafico, specifica il membro **VT** della struttura **Variant** come VT \_ sconosciuto. Se il plug-in fornisce più oggetti di **IStream** grafici utilizzando un SAFEARRAY, specifica il membro **VT** della struttura **Variant** come matrice VT \_ .

La grafica può essere archiviata in diversi formati di file, tra cui:

**BMP**

Le immagini bitmap di Microsoft Windows non sono compresse.

**JPEG**

Formato di immagine compresso usato comunemente per le pagine Web. In genere i file di formato JPEG hanno estensioni di file jpg.

**GIF**

Formato di immagine compresso usato comunemente per le pagine Web.

**PNG**

Formato di immagine compresso usato comunemente per le pagine Web.

Le dimensioni massime per la grafica plug-in DSP sono di 38 pixel di larghezza e 14 pixel di altezza.

Il flusso di byte **IStream** contenente l'elemento grafico di stato deve includere informazioni di intestazione. Senza informazioni di intestazione, Windows Media Player non è in grado di identificare correttamente il tipo di grafico e pertanto non caricherà l'immagine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica per gli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




