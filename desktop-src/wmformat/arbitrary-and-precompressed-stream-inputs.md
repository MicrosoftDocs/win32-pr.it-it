---
title: Input di flusso arbitrario e precompresso
description: Input di flusso arbitrario e precompresso
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- ASF (Advanced Systems Format), input di flusso arbitrario
- ASF (formato avanzato dei sistemi), input di flusso arbitrario
- profili, input di flussi arbitrari
- codec, input di flusso arbitrari
- Advanced Systems Format (ASF), input di flusso precompressi
- ASF (Advanced Systems Format), input di flusso precompressi
- profili, input di flusso precompressi
- codec, input di flusso precompressi
- input di flusso precompressi
- input di flusso arbitrari
- flussi, input di flusso arbitrari
- flussi, input di flusso precompressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1c95fe992c7638ac923ac07ce159fb5dc4126
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "106299509"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a>Input di flusso arbitrario e precompresso

Solo gli input che devono essere compressi da uno dei codec Windows Media hanno più input possibili. Gli altri tipi di input possibili sono input arbitrari e input precompressi. I requisiti per i formati di input per questi tipi sono descritti in questa sezione.

## <a name="arbitrary-stream-inputs"></a>Input di flusso arbitrari

Gli input per i tipi di flusso arbitrari sono identici ai formati di flusso descritti nel profilo. Non è necessario impostare i formati di input per questi tipi.

## <a name="precompressed-stream-inputs"></a>Input di flusso precompressi

Quando si copia un flusso da un file a un altro, si passano esempi già compressi. In questo caso, è necessario impostare l'oggetto proprietà di input su **null** per informare il writer che non è necessario convalidare i dati passati. Per impostare il formato di input su **null**, chiamare [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) e passare **null** come secondo parametro. Quando si chiama questo metodo con un parametro **null** , è necessario effettuare la chiamata prima di chiamare [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

Quando si usano flussi precompressi, è necessario copiare manualmente le informazioni sul codec nell'intestazione del file prima di scrivere. Per ottenere le informazioni sul codec, chiamare [**IWMHeaderInfo2:: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2:: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) per enumerare i codec associati al file nel lettore. Selezionare le informazioni sul codec che corrispondono alla configurazione del flusso del flusso precompresso. Impostare quindi le informazioni sul codec nel writer chiamando [**IWMHeaderInfo3:: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passando le informazioni ottenute dal reader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Utilizzo degli input**](working-with-inputs.md)
</dt> </dl>

 

 




