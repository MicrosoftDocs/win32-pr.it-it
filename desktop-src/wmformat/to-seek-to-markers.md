---
title: Per cercare marcatori
description: Per cercare marcatori
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- Advanced Systems Format (ASF), ricerca di marcatori
- ASF (Advanced Systems Format), ricerca di marcatori
- Advanced Systems Format (ASF), lettori asincroni
- ASF (Advanced Systems Format),lettori asincroni
- Advanced Systems Format (ASF), marcatori
- ASF (Advanced Systems Format), marcatori
- lettori asincroni, ricerca di marcatori
- lettori asincroni, marcatori
- marcatori, ricerca
- marcatori, lettori asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3361546f4087e0c2104809435d9d75e8711560ec4f3c55855d14b05ef4dfb8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807351"
---
# <a name="to-seek-to-markers"></a>Per cercare marcatori

Un marcatore è una posizione denominata in un file ASF. È possibile avviare la riproduzione solo dalla posizione di un marcatore usando il lettore asincrono. È possibile iniziare la riproduzione in corrispondenza di un marcatore seguendo questa procedura.

1.  Chiamare **IWMReader::QueryInterface** per ottenere un puntatore [**all'interfaccia IWMHeaderInfo.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
2.  Recuperare il numero totale di marcatori nel file chiamando [**IWMHeaderInfo::GetMarkerCount.**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount)
3.  Scorrere i marcatori, usando il conteggio dei marcatori recuperato nel passaggio 2. Recuperare il nome e l'ora di ogni marcatore chiamando [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) per ognuno. Salvare l'indice del marcatore desiderato.
4.  Chiamare **IWMReader::QueryInterface** per ottenere un puntatore [**all'interfaccia IWMReaderAdvanced2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
5.  Specificare il marcatore da cui avviare la riproduzione chiamando [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker). È necessario passare l'indice del marcatore desiderato, salvato nel passaggio 3.
6.  Gestire gli esempi come di consueto nell'implementazione del [**metodo IWMReaderCallback::OnSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Marcatori**](markers.md)
</dt> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




