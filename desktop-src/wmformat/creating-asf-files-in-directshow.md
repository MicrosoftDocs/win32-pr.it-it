---
title: Creazione di file ASF in DirectShow (Windows Media Format 11 SDK)
description: Creazione di file ASF in DirectShow
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media Format SDK, creazione di file ASF in DirectShow
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), creazione in DirectShow
- ASF (formato avanzato dei sistemi), creazione in DirectShow
- DirectShow, creazione di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe4a6a37a508e5d7c713ae4cf38d771d075cefa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118770"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a>Creazione di file ASF in DirectShow (Windows Media Format 11 SDK)

È possibile utilizzare DirectShow per creare file ASF direttamente da origini di acquisizione, ad esempio videocamere DV o per la transcodifica di altri file in formato Windows Media. In entrambi gli scenari, le applicazioni creano grafici di filtro che includono il filtro del [writer ASF WM](wm-asf-writer-filter.md) come renderer.

Il writer ASF WM fornisce un wrapper parziale per Windows Media Format SDK. Le applicazioni possono utilizzare l'interfaccia [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) del filtro per passare un profilo di sistema (versioni 4, 7 o 8) oppure utilizzare direttamente Windows Media Format SDK per creare un profilo personalizzato da passare al filtro. Per aggiungere metadati e altre informazioni di intestazione, l'applicazione utilizza l'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , che può essere ottenuta dal filtro. Dopo aver configurato il profilo e i metadati, l'applicazione può semplicemente eseguire il grafico del filtro. Internamente, il filtro usa Windows Media Format SDK per scrivere il file. Il filtro gestisce tutti i dettagli della sincronizzazione del video audio, che altrimenti sarebbero la responsabilità dell'applicazione.

Questo processo viene illustrato più dettagliatamente nelle sezioni seguenti.



| Sezione                                                                                                           | Descrizione                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Configurazione del writer ASF WM (QASF)](configuring-the-wm-asf-writer--qasf.md)                                   | Viene descritto come configurare il filtro del writer ASF WM.                                   |
| [Creazione di grafici di filtro per la scrittura di file ASF (QASF)](building-filter-graphs-to-write-asf-files--qasf.md)           | Viene descritto come creare una transcodifica di file e acquisire grafici.                           |
| [Configurazione di profili e altre proprietà di file (QASF)](configuring-profiles-and-other-file-properties--qasf.md) | Viene descritto come eseguire varie attività di configurazione di file ASF usando il writer ASF WM. |



 

 

 
