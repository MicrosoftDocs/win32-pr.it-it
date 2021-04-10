---
description: Esempio ASFParser
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: Esempio ASFParser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159b481e22d77b0bee9adccbbb74073398c12b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225838"
---
# <a name="asfparser-sample"></a>Esempio ASFParser

Viene illustrato come analizzare i dati da un file Advanced Systems Format (ASF) utilizzando i componenti ASF di basso livello in Media Foundation. Nell'esempio vengono illustrate le attività seguenti:

-   Enumerazione dei flussi audio e video in un file ASF.
-   Selezione di un flusso audio o video per l'analisi.
-   Ricerca di un pacchetto al momento della riproduzione desiderata.
-   Generazione di esempi compressi per il flusso selezionato.
-   Decodifica di esempi audio e video.

## <a name="apis-demonstrated"></a>API illustrate

In questo esempio vengono illustrate le interfacce Microsoft Media Foundation seguenti:

-   [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a>Utilizzo

1.  Per aprire un file ASF, fare clic sul pulsante **Apri file multimediale...** .
2.  Selezionare un file ASF e fare clic su **Apri**. Le informazioni sul file vengono visualizzate nel riquadro **informazioni** .
3.  In **configurazione parser** selezionare un flusso da analizzare.
4.  Per generare gli esempi in ordine inverso, selezionare **Inverti**.
5.  Per specificare il punto iniziale, trascinare il dispositivo di scorrimento nella posizione desiderata.
6.  Per iniziare l'analisi, fare clic sul pulsante **genera esempi** . Le informazioni sugli esempi sono visualizzate nel riquadro **informazioni** .
7.  Per testare gli esempi per il flusso audio, fare clic sul pulsante **prova audio** .
8.  Per testare gli esempi per il flusso video, fare clic sul pulsante **Mostra bitmap** .

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Esercitazione: lettura di un file ASF](tutorial--reading-an-asf-file.md)
</dt> <dt>

[Componenti ASF WMContainer](wmcontainer-asf-components.md)
</dt> </dl>

 

 



