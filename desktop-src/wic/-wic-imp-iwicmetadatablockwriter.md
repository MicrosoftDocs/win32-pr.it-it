---
description: Implementazione di IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Implementazione di IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62044ce9695a45a8fe052d67479158aa9e4baf6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530270"
---
# <a name="implementing-iwicmetadatablockwriter"></a>Implementazione di IWICMetadataBlockWriter

## <a name="iwicmetadatablockwriter"></a>IWICMetadataBlockWriter

-   [InitializeFromBlockReader](#initializefromblockreader)
-   [GetWriterByIndex](#getwriterbyindex)
-   [AddWriter](#addwriter)
-   [SetWriterByIndex](#setwriterbyindex)
-   [RemoveWriterByIndex](#removewriterbyindex)

La classe di codifica a livello di frame implementa questa interfaccia per esporre tutti i blocchi di metadati e richiedere il writer di metadati appropriato per ogni blocco. Se il formato dell'immagine supporta i metadati globali, al di fuori di qualsiasi singolo frame, è necessario implementare anche questa interfaccia sulla classe del codificatore a livello di contenitore. Per una descrizione più dettagliata dei gestori di metadati, vedere la sezione in [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) nella sezione relativa all'implementazione di un decodificatore WIC-Enabled.

``` syntax
interface IWICMetadataBlockWriter : IWICMetadataBlockReader
{
   // All methods required
   HRESULT InitializeFromBlockReader ( IWICMetadataBlockReader *pIMDBlockReader );
   HRESULT GetWriterByIndex ( UINT nIndex, IWICMetadataWriter **ppIMetadataWriter );
   HRESULT AddWriter (IWICMetadataWriter *pIMetadataWriter );
   HRESULT SetWriterByIndex ( UINT nIndex, IWICMetadataWriter *pIMetadataWriter );
   HRESULT RemoveWriterByIndex ( UINT nIndex );
}
```

### <a name="initializefromblockreader"></a>InitializeFromBlockReader

[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) usa un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) per inizializzare il writer del blocco. È possibile ottenere il **IWICMetadataBlockReader** dal decodificatore per decodificare l'immagine.


```C++
UINT blockCount = 0;
IWICMetadataReader* pMetadataReader = NULL;
IWICMetadataWriter** ppMetadataWriter = NULL;
HRESULT hr;

hr = m_pBlockReader->GetCount(&blockCount);
ppMetadataWriter = IWICMetadataWriter*[blockCount];

for (UINT x=0; x < blockCount; x++)
{
   hr = m_pBlockReader->GetReaderByIndex(&pMetadataReader);
   hr = m_pComponentFactory->CreateMetadataWriterFromReader(
         pMetadataReader, NULL, &ppMetadataWriter[x]);
}
```



Poiché l'inizializzazione di [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) con un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) crea un'istanza di un writer di metadati per ogni lettore di metadati esposto dall'oggetto **IWICMetadataBlockReader** , l'applicazione non deve richiedere esplicitamente un writer per ogni blocco di metadati.

### <a name="getwriterbyindex"></a>GetWriterByIndex

[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) restituisce l'oggetto [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) per il blocco di metadati nth, dove n è il valore passato nel parametro *nIndex* . Se non è presente alcun writer di metadati registrato in grado di gestire il tipo di metadati nel blocco ennesimo, la factory del componente restituisce il gestore di metadati sconosciuto, che considererà il blocco dei metadati come oggetto binario di grandi dimensioni (BLOB). Verrà serializzato come flusso di bit senza provare ad analizzarlo.

### <a name="addwriter"></a>AddWriter

[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) consente a un chiamante di aggiungere un nuovo writer di metadati. Questa operazione è necessaria se un'applicazione desidera aggiungere metadati di un formato diverso rispetto a qualsiasi blocco di metadati esistente. Ad esempio, un'applicazione potrebbe voler aggiungere alcuni metadati XMP. Se non è presente alcun blocco di metadati XMP, l'applicazione deve creare un'istanza di un writer di metadati XMP e usare il metodo **AddWriter** per includerlo nella raccolta di writer di metadati.

### <a name="setwriterbyindex"></a>SetWriterByIndex

[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) viene utilizzato per aggiungere un writer di metadati in corrispondenza di un indice specifico nella raccolta. Se un writer di metadati è attualmente presente in tale indice, il nuovo deve sostituirlo.

### <a name="removewriterbyindex"></a>RemoveWriterByIndex

[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) viene utilizzato per rimuovere un writer di metadati dalla raccolta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[Installazione e registrazione di CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



