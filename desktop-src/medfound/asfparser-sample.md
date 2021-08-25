---
description: Esempio di ASFParser
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: Esempio di ASFParser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50db441be45d28899bc8f2ace68b8f09af40e679449d26aec7adf25ab4fb9e2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959551"
---
# <a name="asfparser-sample"></a>Esempio di ASFParser

Illustra come analizzare i dati da un file ASF (Advanced Systems Format) usando i componenti ASF di basso livello in Media Foundation. Nell'esempio vengono illustrate le attività seguenti:

-   Enumerazione dei flussi audio e video in un file ASF.
-   Selezione di un flusso audio o video per l'analisi.
-   Ricerca di un pacchetto in un momento di riproduzione desiderato.
-   Generazione di esempi compressi per il flusso selezionato.
-   Decodifica di esempi audio e video.

## <a name="apis-demonstrated"></a>DIMOSTRAZIONE DELLE API

In questo esempio vengono illustrate le Microsoft Media Foundation seguenti:

-   [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a>Utilizzo

1.  Per aprire un file ASF, fare clic **sul pulsante Apri file** multimediale.
2.  Selezionare un file ASF e fare clic su **Apri.** Le informazioni sul file vengono visualizzate nel **riquadro** Informazioni.
3.  In **Configurazione parser** selezionare un flusso da analizzare.
4.  Per generare esempi in ordine inverso, selezionare **Inverti.**
5.  Per specificare il punto iniziale, trascinare il dispositivo di scorrimento nella posizione desiderata.
6.  Per iniziare l'analisi, fare clic **sul pulsante Generate Samples (Genera** esempi). Le informazioni sugli esempi vengono visualizzate nel **riquadro** Informazioni.
7.  Per testare gli esempi per il flusso audio, fare clic sul **pulsante Test Audio (Testa** audio).
8.  Per testare gli esempi per il flusso video, fare clic **sul pulsante Mostra bitmap.**

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository github Windows esempi classici.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Supporto di ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Esercitazione: Lettura di un file ASF](tutorial--reading-an-asf-file.md)
</dt> <dt>

[Componenti ASF WMContainer](wmcontainer-asf-components.md)
</dt> </dl>

 

 



