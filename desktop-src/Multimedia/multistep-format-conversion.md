---
title: Conversione del formato a più passaggi
description: Conversione del formato a più passaggi
ms.assetid: 21d837e7-d665-461d-9676-68add3829fb0
keywords:
- Gestione compressione audio (ACM), conversione dei dati
- ACM (Gestione compressione audio), conversione dei dati
- Esempi di ACM, conversione di dati
- conversione dei dati
- acmFormatSuggest (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e81ebd5bef17d6a97cb5735e15219c39d3116b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955526"
---
# <a name="multistep-format-conversion"></a>Conversione del formato a più passaggi

In alcuni casi l'ACM non è in grado di convertire i dati da un formato a un altro in un singolo passaggio. Ad esempio, un'applicazione potrebbe dover convertire i dati stereo a 16 bit 44-kHz in mono ADPCM a 11 kHz. Se il compressore o il decompressore non è in grado di eseguire direttamente questa conversione, l'applicazione potrebbe tentarla in due passaggi. Ciò significa in genere eseguire una conversione tra due formati PCM, quindi un'altra conversione nel tipo di formato finale.

Per eseguire la conversione in due passaggi, usare la funzione [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) per trovare un formato PCM corrispondente al formato ADPCM. Usare quindi due flussi di conversione per eseguire la conversione. Ad esempio, è possibile eseguire una conversione da PCM stereo a 16 bit, 44-kHz a 16 bit, 11 kHz mono, quindi eseguire la conversione da una mono a 11 kHz e da 11 kHz a 11 kHz mono ADPCM.

La conversione a più passaggi si verifica anche quando il formato di origine o di destinazione non è PCM. Se il formato di origine non è PCM, è necessario modificarlo in un formato PCM prima della conversione. Se il formato di destinazione non è PCM, l'origine deve essere convertita in un formato PCM intermedio e quindi convertita nel formato di destinazione finale.

Le conversioni più semplici si verificano quando i formati di origine e di destinazione sono entrambi formati PCM. Quando il formato di origine o di destinazione non è PCM, la conversione potrebbe richiedere un passaggio aggiuntivo. Se i formati di origine e di destinazione non sono PCM, la conversione richiede in genere più di un passaggio e, in alcuni casi, la conversione potrebbe non essere possibile.

 

 




