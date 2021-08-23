---
title: Input di flusso arbitrari e precompressi
description: Input di flusso arbitrari e precompressi
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- Advanced Systems Format (ASF), input di flusso arbitrari
- ASF (Advanced Systems Format), input di flusso arbitrari
- profili, input di flussi arbitrari
- codec, input di flusso arbitrari
- Advanced Systems Format (ASF), input di flusso precompressi
- ASF (Advanced Systems Format), input di flusso precompressi
- profili, input di flussi precompressi
- codec, input di flussi precompressi
- input di flusso precompressi
- input di flussi arbitrari
- flussi, input di flussi arbitrari
- flussi, input di flussi precompressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb0129362e8dc01b7ccf3faabbf10e22ffd4eccc082782796059b3cf4578c33a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448271"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a>Input di flusso arbitrari e precompressi

Solo gli input che devono essere compressi da uno dei codec Windows media hanno più input possibili. Gli altri tipi di input possibili sono input arbitrari e input precompressi. I requisiti per i formati di input per questi tipi sono descritti in questa sezione.

## <a name="arbitrary-stream-inputs"></a>Input di flusso arbitrari

Gli input per i tipi di flusso arbitrari sono gli stessi dei formati di flusso descritti nel profilo. Non è necessario impostare formati di input per questi tipi.

## <a name="precompressed-stream-inputs"></a>Input del flusso precompressi

Quando si copia un flusso da un file a un altro, si passano esempi già compressi. In questo caso, è necessario impostare l'oggetto delle proprietà di input su **NULL** per informare il writer che non è necessario convalidare i dati che si stanno passando. Per impostare il formato di input **su NULL,** chiamare [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) e passare **NULL** come secondo parametro. Quando si chiama questo metodo con **un parametro NULL,** è necessario effettuare la chiamata prima di [**chiamare BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

Quando si usano flussi precompressi, è necessario copiare manualmente le informazioni sul codec nell'intestazione del file prima di scrivere. Per ottenere le informazioni sul codec, chiamare [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) per enumerare i codec associati al file nel lettore. Selezionare le informazioni sul codec che corrispondono alla configurazione del flusso precompresso. Impostare quindi le informazioni sul codec nel writer chiamando [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passando le informazioni ottenute dal lettore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso degli input**](working-with-inputs.md)
</dt> </dl>

 

 




