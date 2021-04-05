---
title: Per eseguire la ricerca in base al numero di frame utilizzando il Reader asincrono
description: Per eseguire la ricerca in base al numero di frame utilizzando il Reader asincrono
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- Formato di sistemi avanzati (ASF), ricerca per numero di frame
- ASF (Advanced Systems Format), ricerca per numero di frame
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- Reader asincroni, ricerca per numero di frame
- flussi video, ricerca per numero di frame
- flussi video, lettori asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 169f5e1ac1e6034bc1db6f610e80af50dd3a0215
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046291"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a>Per eseguire la ricerca in base al numero di frame utilizzando il Reader asincrono

L'oggetto Reader asincrono può essere utilizzato per cercare i numeri di frame dei flussi video in un file ASF. Per usare la ricerca basata su frame, il file caricato nel lettore deve essere indicizzato in base al frame. Ogni singolo flusso video può essere indicizzato. Per determinare se un flusso è stato indicizzato in base al frame, è possibile controllare l' \_ attributo g wszWMNumberOfFrames nell'intestazione del file chiamando [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Per cercare i dati in un file ASF in base al numero di frame usando il Reader asincrono, seguire questa procedura.

1.  Ottenere un puntatore all'interfaccia [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) dell'oggetto Reader chiamando **IWMReader:: QueryInterface**.
2.  Per impostare il numero e la durata del fotogramma iniziale, chiamare [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition). È necessario specificare il numero di flusso di un flusso video indicizzato con frame. Il lettore sincronizza il resto degli output con l'ora di presentazione del frame specificato del flusso specificato e inizia a consegnare gli esempi di output.
3.  Gestire gli esempi normalmente nell'implementazione del metodo **IWMReaderCallback:: OnSample** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lettura dei metadati durante la riproduzione**](reading-metadata-at-playback.md)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




