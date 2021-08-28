---
description: ADPCM (Adaptive Differential Pulse Code Modulation) è un formato di compressione con perdita implementata per XAudio2 per fornire funzionalità aggiuntive per specificare le dimensioni del blocco di esempio di compressione.
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: Panoramica di ADPCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1be1155d6d9f5a542b605c497ce28aa34191c0ac129582c18ec4a47b9f510f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962720"
---
# <a name="adpcm-overview"></a>Panoramica di ADPCM

ADPCM (Adaptive Differential Pulse Code Modulation) è un formato di compressione con perdita implementata per XAudio2 per fornire funzionalità aggiuntive per specificare le dimensioni del blocco di esempio di compressione. Con un formato di compressione con perdita alcuni dati vengono modificati e persi durante la compressione. ADPCM può ottenere rapporti di compressione fino a 4:1.

L'implementazione di ADPCM per XAudio2 offre funzionalità aggiuntive per specificare le dimensioni del blocco di esempio di compressione. ADPCM consente alla finestra di progettazione audio di scegliere un'impostazione che rappresenta un compromesso appropriato tra dimensioni, qualità e risoluzione (per il posizionamento dei punti ciclo).

XAudio2 usa una versione modificata del codec Microsoft ADPCM che supporta la formattazione estesa dei dati necessaria per fornire dimensioni dei blocchi di esempio personalizzate. Per questo motivo, i dati audio XAudio2 non possono essere riprodotti dai motori audio che non supportano questa versione del codec ADPCM.

> [!Note]  
> Attualmente la compressione ADPCM è disponibile solo per Windows, tra cui XNA Game Studio Express per Windows distribuzione.

 

## <a name="adpcm-encoding"></a>Codifica ADPCM

I dati audio vengono codificati in ADPCM usando lo strumento da riga di comando AdpcmEncode.

-   AdpcmEncode

    Per codificare i file audio come ADPCM per l'uso con XAudio2, usare lo strumento da riga di comando **AdpcmEncode.**

## <a name="adpcm-decoding"></a>Decodifica ADPCM

La decodifica software di ADPCM è supportata in XAudio2.

-   XAudio2

    Per usare i dati codificati ad ADPCM in XAudio2, è necessario inizializzare una struttura **ADPCMWAVEFORMAT** con valori specifici di ADPCM e passarla come argomento a [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) quando si crea una voce di origine. Per un esempio di caricamento e riproduzione di un suono in XAudio2, vedere Procedura: Riprodurre un [suono con XAudio2.](how-to--play-a-sound-with-xaudio2.md)

## <a name="samplesperblock"></a>SamplesPerBlock

La compressione ADPCM funziona separando la forma d'onda in blocchi e stimando la variazione dei campioni di forma d'onda all'interno di ogni blocco. Le dimensioni dei blocchi vengono misurate in campioni. La dimensione del blocco più piccola è 32 campioni e la più alta è 512 campioni.

I blocchi più grandi consentono una compressione migliore, che comporta dimensioni di file più piccole, ma a scapito della qualità del suono e della risoluzione per l'allineamento dei punti ciclo.

In generale, la modifica del valore SamplesPerBlock comporta i compromessi seguenti:



| If SamplesPerBlock...      | Compressione file | Qualità del suono | Risoluzione del punto di ciclo |
|----------------------------|------------------|---------------|-----------------------|
| Aumenti (fino al massimo 512)  | Aumenta        | Diminuisce     | Diminuisce             |
| Diminuisce (fino al minimo 32) | Diminuisce        | Aumenta     | Aumenta             |



 

## <a name="restrictions"></a>Restrizioni

Poiché ADPCM usa blocchi di esempio allineati uno dopo l'altro, un'onda compressa con ADPCM può avere un blocco parziale non completo alla fine. Il decodificatore ADPCM genera silenzio per il resto di questo blocco parziale, che impedisce all'ondata di scorrere senza problemi.

Il valore del parametro *SamplesPerBlock* influisce sulla risoluzione con cui è possibile allineare i dati delle onde e i punti del ciclo.

Se si tenta di applicare la compressione a un'onda non allineata, si riceverà un errore o un avviso a seconda che l'ondata sia usata in qualsiasi evento di riproduzione a ciclo continuo. Non è possibile comprimere un'onda usata in qualsiasi evento di riproduzione a ciclo continuo. Rimuoverlo dagli eventi di riproduzione a ciclo continuo e applicare nuovamente la compressione.

Se si usa l'ondata esclusivamente in modalità non ciclo, la restrizione di allineamento dei blocchi di esempio non viene applicata.

## <a name="adpcm-file-structure"></a>Struttura di file ADPCM

Un file ADPCM è un file RIFF standard con i tipi di blocco seguenti.



| Blocco FCC     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RIFF          | Blocco RIFF standard contenente un tipo di file con il valore WAVE nei primi quattro byte della sezione dei dati e gli altri blocchi nel file nella sezione restante dei dati.                                                                                                                                                                                                                                                                 |
| Fmt           | Contiene l'intestazione di formato per il file ADPCM. I dati in questo blocco corrispondono a una **struttura ADPCMWAVEFORMAT.**                                                                                                                                                                                                                                                                                                                             |
| data          | Contiene i dati audio ADPCM codificati. Quando si usa ADPCM in XAudio2, è necessario leggere il contenuto del blocco di dati in un buffer e passarlo a una voce di origine come membro **pAudioData** di una struttura [**BUFFER XAUDIO2. \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Non è necessario scambiare in byte il contenuto del blocco di dati.                                                                                                                            |
| smpl e wsmp | Tipi di blocco facoltativi contenenti le informazioni di ciclo per il file ADPCM. Quando si usa ADPCM in XAudio2, i valori contenuti nei blocchi smpl o wsmp vengono usati per popolare i membri **LoopBeginLoopLength** e **LoopCount** della struttura [**BUFFER XAUDIO2. \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Nel Xbox 360, è necessario scambiare in byte i dati caricati da un blocco smpl per tenere conto della differenza di endianness tra Windows e Xbox 360. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 
