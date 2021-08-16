---
title: Per cercare in base al numero di frame usando il lettore asincrono
description: Per cercare in base al numero di frame usando il lettore asincrono
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- Advanced Systems Format (ASF), ricerca in base ai numeri di frame
- ASF (Advanced Systems Format), ricerca in base ai numeri di frame
- Advanced Systems Format (ASF), lettori asincroni
- ASF (Advanced Systems Format), lettori asincroni
- lettori asincroni, ricerca in base ai numeri di frame
- flussi video, ricerca in base ai numeri di fotogramma
- flussi video, lettori asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e218384b1a27bb3240ac74ad9af6d8298945bb57dfaf635531cb4cbb9aaa9611
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432614"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a>Per cercare in base al numero di frame usando il lettore asincrono

L'oggetto lettore asincrono può essere usato per cercare i numeri di fotogrammi dei flussi video in un file ASF. Per usare la ricerca basata su frame, il file caricato nel lettore deve essere indicizzato in base al frame. Ogni singolo flusso video può essere indicizzato. Per determinare se un flusso è stato indicizzato in base al frame, è possibile controllare l'attributo \_ g wszWMNumberOfFrames nell'intestazione del file chiamando [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Per cercare i dati in un file ASF in base al numero di frame usando il lettore asincrono, seguire questa procedura.

1.  Ottenere un puntatore [**all'interfaccia IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) dell'oggetto reader chiamando **IWMReader::QueryInterface**.
2.  Impostare il numero di frame iniziale e la durata chiamando [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition). È necessario specificare il numero di flusso di un flusso video indicizzato con frame. Il lettore sincronirà il resto degli output con l'ora di presentazione del frame specificato del flusso specificato e inizierà a fornire gli esempi di output.
3.  Gestire gli esempi come si farebbe normalmente nell'implementazione del **metodo IWMReaderCallback::OnSample.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lettura dei metadati in fase di riproduzione**](reading-metadata-at-playback.md)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




