---
title: Per cercare i marcatori
description: Per cercare i marcatori
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- Formato di sistemi avanzati (ASF), ricerca di marcatori
- ASF (formato avanzato dei sistemi), ricerca di marcatori
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- Advanced Systems Format (ASF), marcatori
- ASF (formato avanzato dei sistemi), marcatori
- Reader asincroni, ricerca di marcatori
- lettori asincroni, marcatori
- marcatori, ricerca
- indicatori, Reader asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16cb4fef99a5c735a12f03f8d2e962d6caf9c2a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "106299526"
---
# <a name="to-seek-to-markers"></a>Per cercare i marcatori

Un marcatore è una posizione denominata in un file ASF. È possibile avviare la riproduzione solo dalla posizione di un marcatore utilizzando il Reader asincrono. È possibile iniziare la riproduzione in corrispondenza di un marcatore attenendosi alla seguente procedura.

1.  Chiamare **IWMReader:: QueryInterface** per ottenere un puntatore all'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) .
2.  Recuperare il numero totale di marcatori nel file chiamando [**IWMHeaderInfo:: GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).
3.  Scorrere i marcatori utilizzando il numero di marcatori recuperato nel passaggio 2. Recuperare il nome e l'ora di ogni marcatore chiamando [**IWMHeaderInfo:: Getmarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) per ognuno di essi. Salvare l'indice del marcatore desiderato.
4.  Chiamare **IWMReader:: QueryInterface** per ottenere un puntatore all'interfaccia [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) .
5.  Specificare il marcatore da cui iniziare la riproduzione chiamando [**IWMReaderAdvanced2:: StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker). È necessario passare l'indice del marcatore desiderato, salvato nel passaggio 3.
6.  Gestire gli esempi normalmente nell'implementazione del metodo [**IWMReaderCallback:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Indicatori**](markers.md)
</dt> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




