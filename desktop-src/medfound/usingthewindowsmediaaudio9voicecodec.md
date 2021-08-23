---
description: Uso del codec Windows Media Audio Voice
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: Uso del codec Windows Media Audio Voice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e53c84a6915b8bc118015f1524e5126085e7ac199cc4726c88739b0a82738d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972670"
---
# <a name="using-the-windows-media-audio-voice-codec"></a>Uso del codec Windows Media Audio Voice

Il codec Windows Media Audio Voice offre una compressione a bassa velocità in bit ottimizzata per l'audio che contiene contenuti vocali. La capacità del codec di produrre campioni di piccole dimensioni è dovuta all'intervallo di frequenza limitato dei suoni della voce umana. Questa ottimizzazione significa che un codificatore vocale dedicato crea un output di scarsa qualità per il contenuto che contiene suoni più complessi, ad esempio musica. Tuttavia, il Windows codec Media Audio Voice compensa questo potenziale problema di qualità fornendo modalità separate per la voce, la musica e il contenuto misto. Il codec analizza il contenuto misto per determinare la modalità da usare per ogni parte del file.

Il codec Windows Media Audio Voice viene implementato nell'oggetto codificatore identificato dall'identificatore di classe CLSID CWMSPEncMediaObject2 e nell'oggetto decodificatore identificato dall'identificatore di classe \_ CLSID \_ CWMSPDecMediaObject. Il tag di formato dei tipi di file multimediali che usano questo codec è 0x00A.

## <a name="configuring-the-encoder"></a>Configurazione del codificatore

Il codificatore vocale supporta tre modalità: voce, musica e mista. Ogni modalità è ottimizzata per ottenere i risultati migliori per quel tipo di contenuto. È possibile configurare la modalità del codificatore vocale usando i metodi di **IPropertyStore** per impostare la proprietà [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode.](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md)

Se configurato per il contenuto misto, Windows codec Media Audio Voice rileverà automaticamente i passi della musica nel contenuto. Se non si è soddisfatti dei risultati, è possibile specificare la posizione della musica nel contenuto usando un elenco di decisioni di modifica (EDL). Per altre informazioni, vedere [Uso di un elenco di decisioni di modifica per la codifica vocale.](usingavoiceeditingdecisionlist.md)

A differenza degli altri codificatori audio, è possibile impostare il valore della finestra del buffer per il contenuto vocale usando la proprietà [MFPKEY \_ WMAVOICE \_ ENC \_ BufferWindow.](mfpkey-wmavoice-enc-bufferwindowproperty.md) Tuttavia, i valori predefiniti dovrebbero funzionare correttamente nella maggior parte dei casi.

> [!Note]  
>    Quando si configura il codificatore vocale, è molto importante impostare il tipo di output prima di impostare il tipo di input. Questo è l'ordine di operazioni consigliato per tutti i codec audio, ma il codificatore vocale può segnalare tipi di output erre se viene impostato un input quando si chiama **IMediaObject::GetOutputType** o **IMFTransform::GetOutputType**.

 

## <a name="decoding"></a>Decodifica

Non esistono requisiti speciali per la decodifica dell'audio vocale. Per altre informazioni, vedere [Configurazione della decodifica audio.](configuringaudiodecoding.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'audio](workingwithaudio.md)
</dt> </dl>

 

 



