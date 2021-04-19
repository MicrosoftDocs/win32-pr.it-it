---
title: Creazione di grafici di filtro per la scrittura di file ASF (QASF)
description: Creazione di grafici di filtro per la scrittura di file ASF (QASF)
ms.assetid: 45583c97-4e59-4a6a-987b-5486e6f33990
keywords:
- Windows Media Format SDK, creazione di grafici di filtro (QASF)
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, scrittura di file ASF (QASF)
- ASF (Advanced Systems Format), creazione di grafici di filtri (QASF)
- ASF (Advanced Systems Format), compilazione di grafici di filtro (QASF)
- Formato Advanced Systems (ASF), scrittura (QASF)
- ASF (Advanced Systems Format), scrittura (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, creazione di grafici di filtri (QASF)
- DirectShow, scrittura di file ASF (QASF)
- Windows Media Format SDK, QASF
- Formato Advanced Systems (ASF), QASF
- ASF (formato avanzato dei sistemi), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbf0a261d1502f76cebc0eb2141cd230c509029
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297743"
---
# <a name="building-filter-graphs-to-write-asf-files-qasf"></a>Creazione di grafici di filtro per la scrittura di file ASF (QASF)

Le applicazioni basate su DirectShow usano in genere uno dei tre tipi di grafico di filtro durante la creazione di contenuto basato su Windows Media:

-   Filtrare i grafici per la conversione o la transcodifica del contenuto da un altro formato in formato Windows Media.
-   Filtrare i grafici per l'inserimento di contenuto non basato su Windows Media (formati di flusso nativo) in file ASF.
-   Filtrare i grafici per l'acquisizione dei dati dinamici e codificarli immediatamente nel formato Windows Media prima di salvarli su disco.

Ogni tipo di grafico di filtro viene descritto più dettagliatamente nelle sezioni seguenti.



| Sezione                                                                                                             | Descrizione                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Transcodifica di file (QASF)](transcoding-files--qasf.md)                                                             | Viene descritto come creare grafici di filtri per la transcodifica di file.                                               |
| [Inserimento di formati di flusso nativi in file ASF (QASF)](inserting-native-stream-formats-into-asf-files--qasf.md)   | Viene descritto come inserire qualsiasi tipo di dati audio o video compressi o non compressi in un file ASF. |
| [Acquisizione diretta da un dispositivo a un file ASF (QASF)](capturing-directly-from-a-device-to-an-asf-file--qasf.md) | Viene descritto come creare grafici del filtro di acquisizione che restituiscono un file ASF.                             |



 

 

 




