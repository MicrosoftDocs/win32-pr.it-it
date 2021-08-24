---
title: Query su linee e controlli audio
description: Query su linee e controlli audio
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- audio multimediale, controlli mixer
- audio, controlli mixer
- mixer audio, linee audio
- linee audio
- mixer audio, controlli
- mixer, controlli
- mixer, linee audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c417b55273ba3f7f96cd857979c73003ed0f88c2161e1c2ac14d934fddcff1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692111"
---
# <a name="audio-line-and-control-queries"></a>Query su linee e controlli audio

I servizi mixer forniscono funzioni per determinare le informazioni sulle linee audio, i controlli delle linee audio e i dettagli dei controlli. I servizi forniscono anche funzioni per l'impostazione dei dettagli di controllo.

È possibile usare la [**funzione mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) per recuperare informazioni su una linea audio specificata. Questa funzione riempie la [**struttura MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) per una linea audio di origine, una linea audio di destinazione o un identificatore di riga specificato. La struttura include il numero di riga di destinazione, il numero di canali nella linea audio, nonché un nome breve e lungo per la linea audio.

La [**funzione mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) recupera informazioni generali su uno o più controlli associati a una linea audio. Questa funzione riempie la [**struttura MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) con informazioni sul controllo o sui controlli specificati. È possibile usare **mixerGetLineControls per** recuperare le proprietà del controllo per uno degli elementi seguenti:

-   Tutti i controlli per una riga di origine specificata
-   Controllo specificato per una riga di origine specificata
-   Primo controllo di una classe specifica per una riga di origine specificata

La [**funzione mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) recupera le proprietà di un singolo controllo associato a una linea audio. Questa funzione riempie la [**struttura MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) con i valori correnti per un controllo.

La [**funzione mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) usa il contenuto della **struttura MIXERCONTROLDETAILS** per impostare le proprietà del controllo specificato. È necessario assicurarsi che tutti i membri di questa struttura siano riempiti prima di chiamare **mixerSetControlDetails**.

 

 