---
title: Creazione di file ASF in DirectShow (Windows Media Format 11 SDK)
description: Informazioni sulla creazione di file ASF in DirectShow usando l'SDK Windows Media Format 11. ASF è un formato di contenitore che può contenere qualsiasi tipo di dati.
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media Format SDK, creazione di file ASF in DirectShow
- Windows Media Format SDK,DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), creazione in DirectShow
- ASF (Advanced Systems Format), creazione in DirectShow
- DirectShow,creazione di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257b62be20ddc2399d43aaac52b6b4ee949e6dfcf3e6e9b486b869d162429c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655746"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a>Creazione di file ASF in DirectShow (Windows Media Format 11 SDK)

È possibile usare DirectShow per creare file ASF direttamente da origini di acquisizione, ad esempio videocamere DV o per transcodificare altri file in Windows Media Format. In entrambi gli scenari, le applicazioni creano grafici di filtro che includono il filtro [WM ASF Writer](wm-asf-writer-filter.md) come renderer.

WM ASF Writer fornisce un wrapper parziale per Windows Media Format SDK. Le applicazioni possono usare l'interfaccia [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) del filtro per passare un profilo di sistema (versioni 4, 7 o 8) o usare direttamente Windows Media Format SDK per creare un profilo personalizzato da passare al filtro. Per aggiungere metadati e altre informazioni sull'intestazione, l'applicazione usa [**l'interfaccia IWMHeaderInfo,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) che può essere ottenuta dal filtro. Dopo aver configurato il profilo e i metadati, l'applicazione può semplicemente eseguire il grafico dei filtri. Internamente, il filtro usa il Windows Media Format SDK per scrivere il file. Il filtro gestisce tutti i dettagli di sincronizzazione audio-video, che altrimenti sarebbero responsabilità dell'applicazione.

Questo processo è illustrato in modo più dettagliato nelle sezioni seguenti.



| Sezione                                                                                                           | Descrizione                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Configurazione di WM ASF Writer (QASF)](configuring-the-wm-asf-writer--qasf.md)                                   | Viene descritto come configurare il filtro WM ASF Writer.                                   |
| [Compilazione di grafici di filtro per la scrittura di file ASF (QASF)](building-filter-graphs-to-write-asf-files--qasf.md)           | Viene descritto come creare grafici di transcoding e acquisizione di file.                           |
| [Configurazione di profili e altre proprietà di file (QASF)](configuring-profiles-and-other-file-properties--qasf.md) | Viene descritto come eseguire varie attività di configurazione di file ASF usando WM ASF Writer. |



 

 

 
