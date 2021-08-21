---
description: Viene descritto come aggiungere estensioni di unità dati quando si usano Windows codificatori multimediali.
ms.assetid: fdadcb85-c564-4d05-a4d7-af53a0107455
title: Uso delle estensioni per unità dati (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4680626f06c93e63f293699360d98ac995eedc3b3351fe617c182dbc176165ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972720"
---
# <a name="using-data-unit-extensions-microsoft-media-foundation"></a>Uso delle estensioni per unità dati (Microsoft Media Foundation)

I Windows codec Audio e Video multimediali sono progettati per funzionare correttamente con il contenitore ASF (Advanced Systems Format). ASF è il formato strutturato usato per Windows file WMA (Media Audio) e file Windows Media Video (WMV). Si tratta di un formato estendibile progettato per lo streaming dei dati. Una delle caratteristiche insolite della struttura di ASF è la possibilità di associare metadati a singoli campioni e di incorporare i dati con gli esempi nel flusso di bit. Un elemento di metadati archiviato in questo modo è denominato estensione *di unità dati* o estensione di *esempio*.

Un'estensione per unità dati può contenere informazioni richieste dal codificatore, dal decodificatore o dall'applicazione lettore. La maggior parte dei tipi di estensione di unità dati implementati nel codec Windows Media 9 Series contiene dati destinati all'applicazione che decodifica ed esegue il rendering dei supporti. Ad esempio, è possibile gestire i codici di ora SMPTE dai dati di origine aggiungendoli come estensioni di unità dati. Tuttavia, le funzionalità del codec seguenti richiedono estensioni per unità dati:

-   [Inserimento forzato di fotogrammi chiave](forcedkeyframeinsertion.md)
-   [Codifica video interlacciata](interlacedvideoencoding.md)
-   La difficoltà nell'uso delle estensioni delle unità dati quando si accede direttamente al codec è il meccanismo tramite il quale l'oggetto riceve i dati dell'estensione. A tale scopo, gli oggetti di Windows Media Format SDK usano oggetti buffer progettati per supportare questa funzionalità. È consigliabile usare Windows Media Format SDK per attivare le funzionalità del codec che richiedono estensioni di unità dati, ma è possibile fare in modo che queste funzionalità funzionino con gli oggetti codec autonomi.

## <a name="passing-extended-samples-to-the-codec-objects"></a>Passaggio di esempi estesi agli oggetti codec

L Windows Media Format SDK usa oggetti buffer che espongono [**interfacce INSSBuffer.**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) L'interfaccia più recente [**è INSSBuffer4.**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) Per passare esempi a un oggetto codec con estensioni per unità dati, è necessario usare un oggetto buffer che implementa [**l'interfaccia IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) o [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) e l'interfaccia **INSSBuffer.** A tale scopo, è possibile usare gli oggetti buffer creati da Windows Media Format SDK o Microsoft Media Foundation oppure creare una classe di buffer personalizzata che soddisfi i requisiti. Per creare una classe di buffer personalizzata, è necessario essere conformi ai prototipi di metodo per le **interfacce INSSBuffer.** Queste definizioni di interfaccia sono disponibili nel file di intestazione wmsbuffer.h installato con Windows Media Format SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 
