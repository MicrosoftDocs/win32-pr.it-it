---
title: Query di controllo e linea audio
description: Query di controllo e linea audio
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- audio multimediale, controlli Mixer
- audio, controlli Mixer
- mixer audio, linee audio
- linee audio
- mixer audio, controlli
- mixer, controlli
- mixer, linee audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec581f2ddb54b06de8fa1a1b1356d9b80422ad5c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725087"
---
# <a name="audio-line-and-control-queries"></a>Query di controllo e linea audio

I servizi mixer forniscono funzioni per determinare le informazioni sulle linee audio, i controlli della linea audio e i dettagli del controllo. I servizi forniscono anche funzioni per l'impostazione dei dettagli del controllo.

È possibile utilizzare la funzione [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) per recuperare informazioni su una linea audio specificata. Questa funzione riempie la struttura [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) per una linea audio di origine, una linea audio di destinazione o un identificatore di riga specificati. La struttura include il numero di riga di destinazione, il numero di canali nella linea audio, oltre a un nome breve e lungo per la linea audio.

La funzione [**mixerGetlineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) recupera informazioni generali su uno o più controlli associati a una linea audio. Questa funzione riempie la struttura [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) con le informazioni sul controllo o sui controlli specificati. È possibile usare **mixerGetlineControls** per recuperare le proprietà dei controlli per uno degli elementi seguenti:

-   Tutti i controlli per una riga di codice sorgente specificata
-   Controllo specificato per una riga di codice sorgente specificata
-   Primo controllo di una classe specifica per una riga di codice sorgente specificata

La funzione [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) recupera le proprietà di un singolo controllo associato a una linea audio. Questa funzione riempie la struttura [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) con i valori correnti per un controllo.

La funzione [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) usa il contenuto della struttura **MIXERCONTROLDETAILS** per impostare le proprietà del controllo specificato. È necessario assicurarsi che tutti i membri di questa struttura vengano riempiti prima di chiamare **mixerSetControlDetails**.

 

 