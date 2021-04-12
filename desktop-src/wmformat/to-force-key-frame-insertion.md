---
title: Per forzare l'inserimento di Key-Frame
description: Per forzare l'inserimento di Key-Frame
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- Formato di sistemi avanzati (ASF), forzatura degli inserimenti di fotogrammi chiave
- ASF (Advanced Systems Format), forzando gli inserimenti di fotogrammi chiave
- ASF (Advanced Systems Format), inserimento di fotogrammi chiave
- ASF (formato avanzato dei sistemi), inserimento di fotogrammi chiave
- fotogrammi chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23006eef1e51d8bc63f2d55cac22e09a2052d83e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104472390"
---
# <a name="to-force-key-frame-insertion"></a>Per forzare l'inserimento di Key-Frame

Il codec Windows Media Video 9 supporta l'inserimento di fotogrammi chiave forzato. Quando si passa un campione al writer, è possibile specificare che deve essere codificato come [*fotogramma chiave*](wmformat-glossary.md).

Per forzare l'inserimento di fotogrammi chiave per un esempio, seguire questa procedura.

1.  Allocare un buffer per contenere l'esempio e recuperare un puntatore all'interfaccia [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) contenente il buffer chiamando [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).
2.  Recuperare il percorso e le dimensioni del buffer creato nel passaggio 1 chiamando [**INSSBuffer:: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).
3.  Copiare i dati di esempio nella posizione del buffer, assicurandosi che l'esempio passato venga inserito nel buffer allocato. A seconda dell'origine degli esempi, è possibile usare un'ampia gamma di funzioni per copiare i dati. Ad esempio, se si copia un flusso da un file AVI, è possibile usare la funzione AVI **AVIStreamRead**.
4.  Aggiornare la quantità di dati utilizzati nel buffer in modo da riflettere le dimensioni effettive dell'esempio chiamando [**INSSBuffer:: selength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).
5.  Ottenere un puntatore all'interfaccia [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) chiamando **INSSBuffer:: QueryInterface**.
6.  Impostare l'esempio come fotogramma chiave forzata chiamando il metodo [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) per impostare la \_ Proprietà WM SampleExtensionGUID \_ OutputCleanPoint. Questa proprietà è un valore booleano. impostarla su **true**.
7.  Passare l'interfaccia del buffer al writer insieme al numero di input e all'ora del campione usando il metodo [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[**Per scrivere esempi**](to-write-samples.md)
</dt> <dt>

[**Codifica della velocità in bit variabile (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




