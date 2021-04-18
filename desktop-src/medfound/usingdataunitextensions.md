---
description: Viene descritto come aggiungere estensioni di unità dati quando si utilizzano codificatori Windows Media.
ms.assetid: fdadcb85-c564-4d05-a4d7-af53a0107455
title: Uso delle estensioni dell'unità dati (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c16053ee078f5adcd48767f53d9e6e1c0eeb02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308979"
---
# <a name="using-data-unit-extensions-microsoft-media-foundation"></a>Uso delle estensioni dell'unità dati (Microsoft Media Foundation)

I codec Windows Media Audio e video sono progettati per funzionare correttamente con il contenitore ASF (Advanced Systems Format). ASF è il formato strutturato usato per i file Windows Media Audio (WMA) e i file di Windows Media Video (WMV). Si tratta di un formato estendibile progettato per la trasmissione di dati. Una delle caratteristiche insolite della struttura ASF è la possibilità di associare metadati a singoli esempi e incorporare tali dati con gli esempi nel flusso di bit. Un elemento dei metadati archiviati in questo modo è denominato estensione di *unità* dati o *estensione di esempio*.

Un'estensione di unità dati può contenere informazioni richieste dal codificatore, dal decodificatore o dall'applicazione Player. La maggior parte dei tipi di estensione di unità dati implementati nella serie di codec Windows Media 9 contiene dati destinati all'applicazione che decodifica ed esegue il rendering del supporto. Ad esempio, è possibile mantenere i codici temporali SMPTE dai dati di origine aggiungendoli come estensioni di unità dati. Tuttavia, le funzionalità di codec seguenti richiedono le estensioni dell'unità dati:

-   [Inserimento fotogramma chiave forzata](forcedkeyframeinsertion.md)
-   [Codifica video interlacciata](interlacedvideoencoding.md)
-   La difficoltà nell'utilizzo delle estensioni dell'unità dati quando si accede direttamente al codec è il meccanismo mediante il quale l'oggetto riceve i dati dell'estensione. Questa operazione viene eseguita dagli oggetti di Windows Media Format SDK utilizzando oggetti buffer progettati per supportare questa funzionalità. Si consiglia di utilizzare Windows Media Format SDK per attivare le funzionalità di codec che richiedono estensioni di unità dati, ma è possibile eseguire queste funzionalità con gli oggetti codec autonomi.

## <a name="passing-extended-samples-to-the-codec-objects"></a>Passaggio di esempi estesi agli oggetti codec

Windows Media Format SDK utilizza oggetti buffer che espongono interfacce [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) . L'interfaccia più recente è [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4). Per passare esempi a un oggetto codec con le estensioni dell'unità dati, è necessario usare un oggetto buffer che implementi l'interfaccia [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) o [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) e l'interfaccia **INSSBuffer** . Per eseguire questa operazione, è possibile usare gli oggetti buffer creati da Windows Media Format SDK o Microsoft Media Foundation oppure è possibile creare una classe di buffer personalizzata che soddisfi i requisiti. Per creare una classe di buffer personalizzata, è necessario conformarsi ai prototipi di metodo per le interfacce **INSSBuffer** . Queste definizioni di interfaccia si trovano nel file di intestazione wmsbuffer. h installato con Windows Media Format SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 
