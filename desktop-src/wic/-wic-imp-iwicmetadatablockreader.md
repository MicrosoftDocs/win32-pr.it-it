---
description: Implementazione di IWICMetadataBlockReader
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: Implementazione di IWICMetadataBlockReader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbb32ca6bf5ce0714c06a6f355c319908c6dd3a61b1ac27f6baf13f6285183ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772261"
---
# <a name="implementing-iwicmetadatablockreader"></a>Implementazione di IWICMetadataBlockReader

## <a name="iwicmetadatablockreader"></a>IWICMetadataBlockReader

All'interno di un'immagine sono spesso presenti più blocchi di metadati, ognuno dei quali espone tipi diversi di informazioni in formati diversi. Nel modello Windows Imaging Component (WIC), i gestori dei metadati sono componenti distinti che, come i decodificatori, sono individuabili in fase di esecuzione. Ogni formato di metadati ha un gestore separato e ognuno di questi gestori di metadati può essere usato con qualsiasi formato di immagine che supporti il formato di metadati gestito. Pertanto, se il formato dell'immagine supporta EXIF, XMP, IPTC o un altro formato, è possibile sfruttare i gestori di metadati standard per questi formati forniti con WIC e non è necessario scriverne uno personalizzato. Naturalmente, se si crea un nuovo formato di metadati, è necessario scrivere un gestore di metadati per esso, che verrà individuato e richiamato in fase di esecuzione esattamente come quelli standard.

> [!Note]  
> Se il formato dell'immagine è basato su un contenitore Tagged Image File Format (TIFF) o JPEG, non sarà necessario scrivere gestori di metadati(a meno che non si sviluppi un formato di metadati nuovo o proprietario). Nei contenitori TIFF e JPEG, i blocchi di metadati si trovano all'interno di IFD e ogni contenitore ha una struttura IFD diversa. WIC fornisce gestori IFD per entrambi questi formati di contenitore che esplorano la struttura IFD e delegano ai gestori di metadati standard per accedere ai metadati al loro interno. Pertanto, se il formato dell'immagine è basato su uno di questi contenitori, è possibile sfruttare automaticamente i gestori IFD WIC. Tuttavia, se si dispone di un formato di contenitore proprietario con una propria struttura di metadati di primo livello univoca, è necessario scrivere un gestore in grado di esplorare la struttura di primo livello e delegare ai gestori di metadati appropriati, proprio come fanno i gestori IFD.

 

Allo stesso modo in cui WIC fornisce un livello di astrazione per le applicazioni che consente loro di lavorare con tutti i formati di immagine nello stesso modo tramite un set coerente di interfacce, WIC fornisce un livello di astrazione per gli autori di codec in relazione ai formati di metadati. Come indicato in precedenza, gli autori di codec in genere non devono lavorare direttamente con i vari formati di metadati che possono essere presenti in un'immagine. Tuttavia, ogni autore di codec è responsabile di fornire un modo per enumerare i blocchi di metadati in modo che sia possibile individuare e creare un'istanza di un gestore di metadati appropriato per ogni blocco.

È necessario implementare questa interfaccia nella classe di decodifica a livello di frame. Potrebbe anche essere necessario implementarlo nella classe del decodificatore a livello di contenitore se il formato dell'immagine espone metadati globali all'esterno di singoli fotogrammi di immagine.

``` syntax
interface IWICMetadataBlockReader : IUnknown
{
   // All methods required
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetCount ( UINT *pcCount );
   HRESULT GetEnumerator ( IEnumUnknown **ppIEnumMetadata );
   HRESULT GetReaderByIndex ( UINT nIndex, IWICMetadataReader **ppIMetadataReader );
}
```

-   [GetContainerFormat](#getcontainerformat)
-   [GetCount](#getcount)
-   [GetEnumerator](#getenumerator)
-   [GetReaderByIndex](#getreaderbyindex)

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat è**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) uguale al metodo [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) nell'implementazione [di IWICBitmapDecoder.](-wic-imp-iwicbitmapdecoder.md)

### <a name="getcount"></a>GetCount

[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) restituisce il numero di blocchi di metadati di primo livello associati al frame.

### <a name="getenumerator"></a>GetEnumerator

[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) restituisce un enumeratore che il chiamante può usare per enumerare i blocchi di metadati nel frame e leggerne i metadati. Per implementare questo metodo, è necessario creare un lettore di metadati per ogni blocco di metadati e implementare un oggetto di enumerazione che enumera la raccolta di lettori di metadati. L'oggetto enumerazione deve [implementare IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) in modo che sia possibile eseguire il cast a IEnumUnknown quando viene restituito nel *parametro ppIEnumMetadata.*

Quando si implementa l'oggetto di enumerazione, è possibile creare tutti i lettori di metadati quando si crea per la prima volta l'oggetto [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) o quando si crea per la prima volta l'oggetto di enumerazione oppure è possibile crearli in modo decompresso all'interno dell'implementazione del [metodo IEnumUnknown::Next.](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) In molti casi, è più efficiente crearli in modalità lazily, ma nell'esempio seguente i lettori di blocchi vengono tutti creati nel costruttore per risparmiare spazio.


```C++
public class MetadataReaderEnumerator : public IEnumUnknown
{
   UINT m_current;
   UINT m_blockCount;
   IWICMetadataReader** m_ppMetadataReader;
   IStream* m_pStream;

   MetadataReaderEnumerator() 
   {
       // Set m_blockCount to the number of metadata blocks in the frame. 
      ...
      m_ppMetadataReader = IWICMetadataReader*[m_blockCount];
       m_current = 0;

      for (UINT x=0; x < m_blockCount; x++) 
      {
         // Find the position in the file where the xth
         // block of metadata lives and seek m_piStream 
         // to that position.
         ...

         m_pComponentFactory->CreateMetadataReaderFromContainer(
            GUID_ContainerFormatTiff,
                        NULL,
                        WICPersistOptions.WICPersistOptionsDefault | 
            WICMetadataCreationOptions.WICMetadataCreationDefault, 
                        m_pStream, &m_ppMetadataReader[x]);
        }
    }

    // Implementation of IEnumUnknown and IUnknown interfaces
    ...
}
```



Per creare i lettori di metadati, usare il [**metodo CreateMetadataReaderFromContainer.**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) Quando si richiama questo metodo, si passa il GUID del formato del contenitore nel *parametro guidContainerFormat.* Se si ha una preferenza di fornitore per un lettore di metadati, è possibile passare il GUID del fornitore preferito nel *parametro pGuidVendor.* Ad esempio, se l'azienda scrive gestori di metadati e si vuole usare il proprio, se presente, è possibile passare il GUID del fornitore. Nella maggior parte dei casi, è sufficiente passare **NULL** e consentire al sistema di selezionare il lettore di metadati appropriato. Se si richiede un fornitore specifico e tale fornitore dispone di un lettore di metadati installato nel computer, wic restituirà il lettore del fornitore. Tuttavia, se il fornitore richiesto non dispone di un lettore di metadati installato nel computer e se è disponibile un lettore di metadati appropriato, tale lettore verrà restituito anche se non è del fornitore preferito. Se nel computer non è presente alcun lettore di metadati per il tipo di metadati nel blocco, la factory dei componenti restituirà il gestore di metadati sconosciuti, che tratterà il blocco di metadati come oggetto binario di grandi dimensioni (BLOB) e deserializzerà il blocco di metadati dal file senza alcun tentativo di analizzarlo.

Per il *parametro dwOptions,* eseguire un'operazione OR tra [**wicPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) appropriato con [**WICMetadataCreationOptions appropriato.**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) **WICPersistOptions** descrive la struttura del contenitore. Little-endian è l'impostazione predefinita.

``` syntax
enum WICPersistOptions
{   
   WICPersistOptionDefault,
   WICPersistOptionLittleEndian,
   WICPersistOptionBigEndian,
   WICPersistOptionStrictFormat,
   WICPersistOptionNoCacheStream,
   WICPersistOptionPreferUTF8
};
```

[**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) specifica se si vuole ottenere nuovamente UnknownMetadataHandler se non viene trovato alcun lettore di metadati nel computer in grado di leggere il formato dei metadati di un blocco specifico. **WICMetadataCreationAllowUnknown** è l'impostazione predefinita ed è consigliabile consentire sempre la creazione di UnknownMetadtataHandler. UnknownMetadataHandler considera i metadati non riconosciuti come BLOB. Non può analizzarlo, ma lo scrive nel flusso come BLOB e lo rende intatto quando viene scritto nel flusso durante la codifica. In questo modo è possibile creare gestori di metadati per metadati proprietari o formati di metadati che non vengono forniti con il sistema. Poiché i metadati vengono mantenuti intatti, anche se nel computer non è presente alcun gestore che lo riconosce, quando in un secondo momento viene installato un gestore di metadati appropriato, i metadati saranno ancora presenti e potranno essere letti. Se non si consente la creazione di UnknownMetadataHandler, l'alternativa consiste nell'eliminare o sovrascrivere i metadati non riconosciuti. Si tratta di una forma di perdita di dati.

> [!Note]  
> Se si scrive un gestore di metadati personalizzato per i metadati proprietari, non includere mai riferimenti a elementi esterni al blocco di metadati stesso. Anche se UnknownMetadataHandler mantiene intatti i metadati, i metadati vengono spostati quando i file vengono modificati e tutti i riferimenti a qualsiasi elemento esterno al proprio blocco non saranno più validi in questo caso.

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

Il *parametro pIStream* è il flusso effettivo che si sta decodificando. Prima di passare il flusso, è necessario cercare l'inizio del blocco di metadati per cui si richiede un lettore. Il lettore di metadati appropriato per il blocco di metadati nella posizione corrente in [IStream](/windows/desktop/api/objidl/nn-objidl-istream) verrà restituito nel *parametro ppiReader.*

### <a name="getreaderbyindex"></a>GetReaderByIndex

[**GetReaderByIndex restituisce**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) il lettore di metadati in corrispondenza dell'indice richiesto nella raccolta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[Implementazione di IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
