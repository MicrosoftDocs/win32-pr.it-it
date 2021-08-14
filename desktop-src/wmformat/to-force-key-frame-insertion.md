---
title: Per forzare lKey-Frame inserimento
description: Per forzare lKey-Frame inserimento
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- Advanced Systems Format (ASF), inserimento forzato di fotogrammi chiave
- ASF (Advanced Systems Format), inserimento forzato di fotogrammi chiave
- Advanced Systems Format (ASF), inserimenti di fotogrammi chiave
- ASF (Advanced Systems Format), inserimenti di fotogrammi chiave
- fotogrammi chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d400c0ee4ba97aa7de559b1394dbe5c9fb2a974c124924aeae0839b1b4dae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196497"
---
# <a name="to-force-key-frame-insertion"></a>Per forzare lKey-Frame inserimento

Il codec Windows Media Video 9 supporta l'inserimento forzato di fotogrammi chiave. Quando si passa un esempio al writer, è possibile specificare che deve essere codificato come [*fotogramma chiave*](wmformat-glossary.md).

Per forzare l'inserimento di fotogrammi chiave per un esempio, seguire questa procedura.

1.  Allocare un buffer per contenere l'esempio e recuperare un puntatore [**all'interfaccia INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) contenente il buffer chiamando [**IWMWriter::AllocateSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample)
2.  Recuperare la posizione e le dimensioni del buffer creato nel passaggio 1 chiamando [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).
3.  Copiare i dati di esempio nella posizione del buffer, assicurando che l'esempio passato si adatti al buffer allocato. A seconda dell'origine degli esempi, è possibile usare un'ampia gamma di funzioni per copiare i dati. Ad esempio, se si copia un flusso da un file AVI, è possibile usare la funzione **AVI, AVIStreamRead.**
4.  Aggiornare la quantità di dati usati nel buffer per riflettere le dimensioni effettive del campione chiamando [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).
5.  Ottenere un puntatore [**all'interfaccia INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) chiamando **INSSBuffer::QueryInterface.**
6.  Impostare l'esempio come fotogramma chiave forzato chiamando il [**metodo INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) per impostare la proprietà \_ OutputCleanPoint di WM \_ SampleExtensionGUID. Questa proprietà è un valore booleano. impostarlo su **TRUE.**
7.  Passare l'interfaccia del buffer al writer insieme al numero di input e all'ora di esempio usando il [**metodo IWMWriter::WriteSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[**Per scrivere esempi**](to-write-samples.md)
</dt> <dt>

[**Codifica vbr (Variable Bit Rate)**](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




