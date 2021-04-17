---
description: Uso del codec Windows Media Audio Voice
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: Uso del codec Windows Media Audio Voice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d636bd97b76e23acc6b68da87c8a206b17dea60a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530468"
---
# <a name="using-the-windows-media-audio-voice-codec"></a>Uso del codec Windows Media Audio Voice

Il codec Windows Media Audio Voice fornisce una compressione a bassa velocità in bit ottimizzata per l'audio che contiene la sintesi vocale. La possibilità che il codec produca questi piccoli esempi è dovuto alla gamma di frequenze limitata dei suoni della voce umana. Questa ottimizzazione significa che un codificatore vocale dedicato crea output di scarsa qualità per contenuti che contengono suoni più complessi, come la musica. Tuttavia, il codec Windows Media Audio Voice compensa questo potenziale problema di qualità fornendo modalità separate per la voce, la musica e il contenuto misto. Il codec analizza il contenuto misto per determinare la modalità da usare per ogni parte del file.

Il codec Windows Media Audio Voice viene implementato nell'oggetto Encoder identificato dall'identificatore di classe CLSID \_ CWMSPEncMediaObject2 e nell'oggetto decodificatore identificato dall'identificatore di classe CLSID \_ CWMSPDecMediaObject. Il tag di formato dei tipi di supporto che usano questo codec è 0x00A.

## <a name="configuring-the-encoder"></a>Configurazione del codificatore

Il codificatore vocale supporta tre modalità: sintesi vocale, musica e mista. Ogni modalità è ottimizzata per ottenere i risultati migliori per quel tipo di contenuto. È possibile configurare la modalità del codificatore vocale usando i metodi di **IPropertyStore** per impostare la proprietà [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) .

Quando è configurato per il contenuto misto, il codec Windows Media Audio Voice rileverà automaticamente i passaggi di musica nel contenuto. Se non si è soddisfatti dei risultati, è possibile specificare la posizione della musica nel contenuto usando un elenco di decisioni di modifica (EDL). Per ulteriori informazioni, vedere [utilizzo di un elenco di decisioni di modifica per la codifica di Voice](usingavoiceeditingdecisionlist.md).

Diversamente dagli altri codificatori audio, è possibile impostare il valore della finestra del buffer per il contenuto vocale usando la proprietà [MFPKEY \_ WMAVOICE \_ enc \_ BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) . Tuttavia, i valori predefiniti dovrebbero funzionare correttamente nella maggior parte dei casi.

> [!Note]  
>    Quando si configura il codificatore vocale, è molto importante impostare il tipo di output prima di impostare il tipo di input. Si tratta dell'ordine delle operazioni consigliato per tutti i codec audio, ma il codificatore vocale può segnalare tipi di output errati se viene impostato un input quando si chiama **IMediaObject:: GetOutputType** o **IMFTransform:: GetOutputType**.

 

## <a name="decoding"></a>Decodifica

Non sono previsti requisiti speciali per la decodifica dell'audio vocale. Per ulteriori informazioni, vedere [configurazione della decodifica audio](configuringaudiodecoding.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di audio](workingwithaudio.md)
</dt> </dl>

 

 



