---
description: La modulazione del codice a impulsi differenziale (ADPCM) è un formato di compressione con perdita di spazio, implementato per XAudio2 per fornire funzionalità aggiuntive per specificare le dimensioni del blocco di esempio di compressione.
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: Panoramica di ADPCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb918a611cb0840b2f02dfb13b547b795fb3304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314430"
---
# <a name="adpcm-overview"></a>Panoramica di ADPCM

La modulazione del codice a impulsi differenziale (ADPCM) è un formato di compressione con perdita di spazio, implementato per XAudio2 per fornire funzionalità aggiuntive per specificare le dimensioni del blocco di esempio di compressione. Con un formato di compressione con perdita di dati, alcuni dati vengono modificati e persi durante la compressione. ADPCM può ottenere rapporti di compressione fino a 4:1.

L'implementazione di ADPCM per XAudio2 fornisce funzionalità aggiuntive per specificare le dimensioni del blocco di esempio di compressione. ADPCM consente alla finestra di progettazione audio di scegliere un'impostazione che rappresenta un compromesso appropriato tra dimensioni, qualità e risoluzione (per l'inserimento di punti di ciclo).

XAudio2 usa una versione modificata del codec Microsoft ADPCM che supporta la formattazione dei dati estesa necessaria per fornire dimensioni del blocco di esempio personalizzate. Per questo motivo, non è possibile riprodurre i dati audio XAudio2 da motori audio che non supportano questa versione del codec ADPCM.

> [!Note]  
> Attualmente, la compressione ADPCM è disponibile solo per Windows, incluse le distribuzioni XNA Game Studio Express per Windows.

 

## <a name="adpcm-encoding"></a>Codifica ADPCM

I dati audio sono codificati in ADPCM usando lo strumento da riga di comando AdpcmEncode.

-   AdpcmEncode

    Per codificare i file audio come ADPCM per l'uso con XAudio2, usare lo strumento da riga di comando **AdpcmEncode** .

## <a name="adpcm-decoding"></a>Decodifica ADPCM

La decodifica software di ADPCM è supportata in XAudio2.

-   XAudio2

    Per usare i dati con codifica ADPCM in XAudio2, è necessario inizializzare una struttura **ADPCMWAVEFORMAT** con valori specifici di ADPCM e passarla come argomento a [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) quando si crea una voce di origine. Per un esempio di caricamento e riproduzione di un suono in XAudio2, vedere [procedura: riprodurre un suono con XAudio2](how-to--play-a-sound-with-xaudio2.md).

## <a name="samplesperblock"></a>SamplesPerBlock

La compressione ADPCM funziona separando la forma d'onda in blocchi e stimando la variazione degli esempi di forma d'onda all'interno di ogni blocco. Le dimensioni dei blocchi sono misurate in esempi. La dimensione minima del blocco è di 32 campioni e la più alta è 512 campioni.

I blocchi di dimensioni maggiori consentono una compressione migliore, che comporta dimensioni di file più ridotte, ma a scapito della qualità e della risoluzione del suono per l'allineamento dei punti del ciclo.

In generale, la modifica del valore di SamplesPerBlock determina i compromessi seguenti:



| Se SamplesPerBlock...      | Compressione file | Qualità audio | Risoluzione del punto di ciclo |
|----------------------------|------------------|---------------|-----------------------|
| Aumenta (fino al massimo 512)  | Aumenta        | Riduce     | Riduce             |
| Diminuisce (fino a min 32) | Riduce        | Aumenta     | Aumenta             |



 

## <a name="restrictions"></a>Restrizioni

Poiché ADPCM utilizza blocchi di esempio che sono allineati uno dopo l'altro, un'onda compressa con ADPCM potrebbe avere un blocco parziale non completato alla fine. Il decodificatore ADPCM genera silenzio per la parte restante del blocco parziale, che impedisce l'iterazione del ciclo in modo uniforme.

Il valore del parametro *SamplesPerBlock* influiscono sulla risoluzione con cui è possibile allineare i dati Wave e i punti di ciclo.

Se si tenta di applicare la compressione a un'onda non allineata, verrà visualizzato un errore o un avviso a seconda che l'onda venga usata in qualsiasi evento di riproduzione del ciclo. Non è possibile comprimere un'onda utilizzata negli eventi di riproduzione del ciclo. Rimuoverlo dagli eventi di riproduzione del ciclo, quindi applicare nuovamente la compressione.

Se si usa l'onda esclusivamente in modalità non di ciclo, la restrizione dell'allineamento del blocco di esempio non si applica.

## <a name="adpcm-file-structure"></a>Struttura di file ADPCM

Un file ADPCM è un file RIFF standard con i tipi di blocchi seguenti.



| Blocco FCC     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RIFF          | Blocco RIFF standard contenente un tipo di file con il valore WAVE nei primi quattro byte della sezione relativa ai dati e gli altri blocchi del file nel resto della sezione relativa ai dati.                                                                                                                                                                                                                                                                 |
| FMT           | Contiene l'intestazione del formato per il file ADPCM. I dati in questo blocco corrispondono a una struttura **ADPCMWAVEFORMAT** .                                                                                                                                                                                                                                                                                                                             |
| data          | Contiene i dati audio ADPCM codificati. Quando si usa ADPCM in XAudio2, è necessario leggere il contenuto del blocco di dati in un buffer e passarlo a una voce di origine come membro **pAudioData** di una struttura di [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . Non è necessario scambiare byte con il contenuto del blocco di dati.                                                                                                                            |
| SMPL e wsmp | Tipi di blocchi facoltativi contenenti le informazioni di ciclo per il file ADPCM. Quando si usa ADPCM in XAudio2, i valori contenuti nei blocchi SMPL o wsmp vengono usati per popolare i membri **LoopBeginLoopLength** e **LoopCount** della struttura del [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . In Xbox 360 è necessario scambiare i dati caricati da un blocco SMPL per tenere conto della differenza di caratteristica tra Windows e Xbox 360. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 
