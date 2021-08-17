---
description: Implementazione di IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Implementazione di IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d49912ece0cc1e3c2299ace0a15f112ef7ab65ac03863b855b8a9ee64e62e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964970"
---
# <a name="implementing-iwicmetadatablockwriter"></a>Implementazione di IWICMetadataBlockWriter

## <a name="iwicmetadatablockwriter"></a>IWICMetadataBlockWriter

-   [InitializeFromBlockReader](#initializefromblockreader)
-   [GetWriterByIndex](#getwriterbyindex)
-   [AddWriter](#addwriter)
-   [SetWriterByIndex](#setwriterbyindex)
-   [RemoveWriterByIndex](#removewriterbyindex)

La classe di codifica a livello di frame implementa questa interfaccia per esporre tutti i blocchi di metadati e richiedere il writer di metadati appropriato per ogni blocco. Se il formato dell'immagine supporta metadati globali, all'esterno di qualsiasi singolo frame, è necessario implementare questa interfaccia anche nella classe del codificatore a livello di contenitore. Per una descrizione più dettagliata dei gestori di metadati, vedere la sezione relativa a [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) nella sezione relativa all'implementazione di un WIC-Enabled decodificatore.

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

[**InitializeFromBlockReader usa**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) un [**oggetto IWICMetadataBlockReader per**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) inizializzare il writer di blocco. È possibile ottenere **IWICMetadataBlockReader dal** decodificatore che ha decodificato l'immagine.


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



Poiché l'inizializzazione di [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) con un oggetto [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) crea un'istanza di un writer di metadati per ogni lettore di metadati esposto dall'oggetto **IWICMetadataBlockReader,** l'applicazione non deve richiedere in modo esplicito un writer per ogni blocco di metadati.

### <a name="getwriterbyindex"></a>GetWriterByIndex

[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) restituisce [**l'oggetto IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) per l'eesimo blocco di metadati, dove n è il valore passato nel *parametro nIndex.* Se non è registrato alcun writer di metadati in grado di gestire il tipo di metadati nel blocco n, la factory dei componenti restituirà il gestore di metadati sconosciuto, che tratterà il blocco di metadati come oggetto binario di grandi dimensioni (BLOB). Lo serializza come flusso di bit senza tentare di analizzarlo.

### <a name="addwriter"></a>AddWriter

[**AddWriter consente**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) a un chiamante di aggiungere un nuovo writer di metadati. Questa operazione è necessaria se un'applicazione desidera aggiungere metadati di un formato diverso rispetto a uno dei blocchi di metadati esistenti. Ad esempio, un'applicazione potrebbe voler aggiungere alcuni metadati XMP. Se non esiste alcun blocco di metadati XMP esistente, l'applicazione deve creare un'istanza di un writer di metadati XMP e usare il **metodo AddWriter** per includerlo nella raccolta di writer di metadati.

### <a name="setwriterbyindex"></a>SetWriterByIndex

[**SetWriterByIndex viene**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) usato per aggiungere un writer di metadati in corrispondenza di un indice specifico nella raccolta. Se in corrispondenza di tale indice è attualmente presente un writer di metadati, il nuovo writer deve sostituirlo.

### <a name="removewriterbyindex"></a>RemoveWriterByIndex

[**RemoveWriterByIndex viene**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) usato per rimuovere un writer di metadati dalla raccolta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[Installazione e registrazione di CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Cenni preliminari sul componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



