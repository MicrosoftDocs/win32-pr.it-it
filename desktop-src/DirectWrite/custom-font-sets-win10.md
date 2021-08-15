---
title: Set di caratteri personalizzati
description: Questo argomento descrive diversi modi in cui è possibile usare tipi di carattere personalizzati nell'app.
ms.assetid: 50842838-d150-df9a-f1b7-67ce5ea2bc80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4b8b9c49895c2b137aaa33cf0788d9518a1d53834c74eb27feb6b44fa045d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650285"
---
# <a name="custom-font-sets"></a>Set di caratteri personalizzati

Questo argomento descrive diversi modi in cui è possibile usare tipi di carattere personalizzati nell'app.

-   [Introduzione ](#introduction)
-   [Riepilogo delle API](#summary-of-apis)
-   [Concetti chiave](#key-concepts)
-   [Tipi di carattere e formati di file dei tipi di carattere](#fonts-and-font-file-formats)
-   [Set di caratteri e raccolte di tipi di carattere](#font-sets-and-font-collections)
-   [Scenari comuni](#common-scenarios)
    -   [Creazione di un set di tipi di carattere usando tipi di carattere arbitrari nel file system](#creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system)
    -   [Creazione di un set di tipi di carattere usando tipi di carattere noti nell'area file system](#creating-a-font-set-using-known-fonts-in-the-local-file-system)
    -   [Creazione di un set di caratteri personalizzato usando tipi di carattere remoti noti sul Web](#creating-a-custom-font-set-using-known-remote-fonts-on-the-web)
    -   [Creazione di un set di tipi di carattere personalizzato usando i dati dei tipi di carattere caricati in memoria](#creating-a-custom-font-set-using-font-data-loaded-into-memory)
-   [Scenari avanzati](#advanced-scenarios)
    -   [Combinazione di set di caratteri](#combining-font-sets)
    -   [Uso dei dati del tipo di carattere WOFF o WOFF2 locali ](#using-local-woff-or-woff2-font-data)
    -   [Uso DirectWrite dei tipi di carattere remoti con l'implementazione di rete di basso livello personalizzata](#using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation)
    -   [Scenari di supporto nelle versioni Windows precedenti](#supporting-scenarios-on-earlier-windows-versions)

## <a name="introduction"></a>Introduzione

Nella maggior parte dei casi, le app usano i tipi di carattere installati localmente nel sistema. DirectWrite l'accesso a questi tipi di carattere usando i metodi [**IDWriteFactory3::GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) [**o IDWriteFactory::GetSystemFontCollection.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) In alcuni casi, è anche possibile che le app vogliano usare tipi di carattere inclusi come parte di Windows 10 ma che non sono attualmente installati nel sistema corrente. È possibile accedere a tali tipi di carattere dal servizio dei tipi di carattere Windows usando il metodo **GetSystemFontSet** o chiamando [**IDWriteFactory3::GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection) con includeDownloadableFonts impostato su TRUE. 

In alcuni scenari applicativi, tuttavia, le app devono usare tipi di carattere che non sono installati nel sistema e non sono forniti dal Windows Font Service. Di seguito sono riportati esempi di tali scenari:

-   I tipi di carattere vengono incorporati come risorse all'interno di un file binario dell'app.
-   I file dei tipi di carattere vengono aggregati all'interno di un pacchetto dell'app e archiviati su disco nella cartella di installazione dell'app.
-   L'app è uno strumento di sviluppo dei tipi di carattere che deve caricare i file dei tipi di carattere specificati dall'utente. 
-   I tipi di carattere sono incorporati nei file di documento che possono essere visualizzati o modificati nell'app. 
-   L'app usa i tipi di carattere ottenuti da un servizio di tipi di carattere Web pubblico. 
-   L'app usa i dati dei tipi di carattere trasmessi tramite un protocollo di rete privato. 

DirectWrite offre API per l'uso di tipi di carattere personalizzati in questi e in altri scenari simili. I dati dei tipi di carattere personalizzati possono derivare da file nel file system; da origini remote basate sul cloud a cui si accede tramite HTTP; o da origini arbitrarie dopo essere state caricate in un buffer di memoria. 

> [!Note]  
> Anche se DirectWrite ha fornito API per l'uso di tipi di carattere personalizzati a partire da Windows 7, sono state aggiunte API più nuove in Windows 10 e di nuovo nel Windows 10 Creators Update (build di anteprima 15021 o successiva) che semplificano l'implementazione di diversi degli scenari indicati. Questo argomento è in particolare sulle API disponibili in Windows 10. Per le applicazioni che devono funzionare in versioni Windows precedenti, vedere Raccolte di tipi di [carattere personalizzati (Windows 7/8).](custom-font-collections.md) 

 

## <a name="summary-of-apis"></a>Riepilogo delle API

Questo argomento è in particolare sulle funzionalità fornite dalle API seguenti: 

-   [**Interfaccia IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
-   [**Interfaccia IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
-   [**Interfaccia IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) 
-   [**Interfaccia IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)
-   [**Interfaccia IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)
-   [**Metodo IDWriteFactory::CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) 
-   [**Metodo IDWriteFactory::CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) 
-   [**Metodi IDWriteFactory3::CreateFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontresource-createfontfacereference) 
-   [**DWRITE \_ Struttura FONT \_ PROPERTY**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) 
-   [**DWRITE \_ Enumerazione FONT \_ PROPERTY \_ ID**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) 
-   [**Interfaccia IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) 
-   [**Metodo IDWriteFactory::RegisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader) 
-   [**Metodo IDWriteFactory::UnregisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontfileloader) 
-   [**Metodo IDWriteFactory5::CreateInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createinmemoryfontfileloader) 
-   [**Interfaccia IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) 
-   [**Metodo IDWriteFactory5::CreateHttpFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createhttpfontfileloader) 
-   [**Interfaccia IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) 
-   [**Interfaccia IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) 
-   [**Interfaccia IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) 
-   [**Interfaccia IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 
-   [**Interfaccia IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) 
-   [**Interfaccia IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) 
-   [**Metodo IDWriteFactory5::AnalyzeContainerType**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-analyzecontainertype) 
-   [**Metodo IDWriteFactory5::UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile) 

 

## <a name="key-concepts"></a>Concetti chiave

Per comprendere le DirectWrite per l'uso di tipi di carattere personalizzati, può essere utile comprendere il modello concettuale alla base di queste API. I concetti chiave verranno descritti qui. 

Quando DirectWrite il layout di testo o il rendering effettivo, deve accedere ai dati effettivi del tipo di carattere. Un oggetto viso del tipo di carattere contiene i dati effettivi del tipo di carattere, che devono esistere nel sistema locale. Per altre operazioni, ad esempio la verifica della disponibilità di un tipo di carattere specifico o la presentazione di scelte di tipi di carattere a un utente, è necessario solo un riferimento a un tipo di carattere specifico, non ai dati effettivi del tipo di carattere stesso. In DirectWrite un oggetto riferimento al viso del tipo di carattere contiene solo le informazioni necessarie per individuare e creare un'istanza di un tipo di carattere. Poiché il riferimento al viso del tipo di carattere non contiene dati effettivi, DirectWrite può gestire i riferimenti ai visi per i quali i dati effettivi si trovano in un percorso di rete remoto e quando i dati effettivi sono locali.

Un set di tipi di carattere è un set di riferimenti al tipo di carattere, insieme ad alcune proprietà in formato informativo di base che possono essere usate per fare riferimento al tipo di carattere o per confrontarlo con altri tipi di carattere, ad esempio il nome della famiglia o un valore di spessore del carattere. I dati effettivi per i vari tipi di carattere possono essere locali, tutti remoti o una combinazione.

Un set di tipi di carattere può essere usato per ottenere un oggetto raccolta di tipi di carattere corrispondente. Per altri dettagli, vedere Set di caratteri e raccolte di tipi di carattere più avanti. 

L'interfaccia IDWriteFontSet fornisce metodi che consentono l'esecuzione di query per i valori delle proprietà, ad esempio il nome della famiglia o lo spessore del carattere, o per i riferimenti ai visi dei caratteri che corrispondono a determinati valori di proprietà. Dopo l'applicazione di un filtro a una selezione specifica, è possibile ottenere un'istanza dell'interfaccia [**IDWriteFontFaceReference,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) con metodi per il download (se i dati effettivi del tipo di carattere sono attualmente remoti), per ottenere l'oggetto [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) corrispondente che può essere usato per il layout e il rendering. 

L'interfaccia IDWriteFontFile è alla base di ogni tipo di carattere o riferimento al viso del tipo di carattere. Rappresenta il percorso di un file del tipo di carattere e include due componenti: un caricatore del file del tipo di carattere e una chiave del file del tipo di carattere. Il caricatore del file del tipo di carattere ([**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)) viene usato per aprire un file, se necessario, e restituisce un flusso con i dati ([**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)). A seconda del caricatore, i dati possono trovarsi in un percorso di file locale, in un URL remoto o in un buffer di memoria. La chiave è un valore definito dal caricatore che identifica in modo univoco il file all'interno del contesto del caricatore, consentendo al caricatore di individuare i dati e creare un flusso per tale file. 

I tipi di carattere personalizzati possono essere facilmente aggiunti a un set di tipi di carattere personalizzato, che a sua volta può essere usato per filtrare o organizzare le informazioni sui tipi di carattere per scopi quali la creazione di un'interfaccia utente di selezione dei caratteri. Il set di caratteri può essere usato anche per creare una raccolta di tipi di carattere da usare in API di livello superiore come [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) [**L'interfaccia IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) può essere usata per creare un set di tipi di carattere personalizzato che include diversi tipi di carattere personalizzati. Può anche essere usato per creare un set di tipi di carattere personalizzato che combina tipi di carattere personalizzati e tipi di carattere forniti dal sistema; o che combina tipi di carattere con origini diverse per i dati effettivi: archiviazione locale, URL remoti e memoria. 

Come accennato, un riferimento al tipo di carattere può fare riferimento ai dati del tipo di carattere in un'origine remota, ma i dati devono essere locali per ottenere un oggetto tipo di carattere che può essere usato per il layout e il rendering. Il download dei dati remoti viene gestito da una coda di download dei tipi di carattere. Le app possono usare l'interfaccia [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) per accodare le richieste di download dei tipi di carattere remoti per avviare il processo di download e per registrare un oggetto [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) per intervenire al termine del processo di download. 

Per la maggior parte delle interfacce descritte qui, DirectWrite implementazioni di sistema. L'unica eccezione è [**l'interfaccia IDWriteFontDownloadListener,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) implementata da un'app per eseguire azioni specifiche dell'app quando i tipi di carattere remoti sono stati scaricati in locale. Le app possono avere motivo di fornire le proprie implementazioni personalizzate per alcune altre interfacce, anche se questo sarebbe necessario solo in scenari specifici e più avanzati. Ad esempio, un'app deve fornire un'implementazione personalizzata dell'interfaccia [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) per gestire i file dei tipi di carattere nell'archiviazione locale che usano il formato contenitore WOFF2. Altri dettagli verranno forniti di seguito. 

## <a name="fonts-and-font-file-formats"></a>Tipi di carattere e formati di file dei tipi di carattere

Un altro concetto chiave utile da comprendere è la relazione tra i singoli visi e i file dei tipi di carattere che li contengono. L'idea di un file di tipo di carattere OpenType (con estensione ttf o otf) contenente un singolo tipo di carattere è familiare. Tuttavia, il formato del tipo di carattere OpenType consente anche una raccolta di tipi di carattere OpenType (TTC o OTC), ovvero un singolo file che contiene più tipi di carattere. I file della raccolta OpenType vengono spesso usati per tipi di carattere di grandi dimensioni strettamente correlati e con valori identici per determinati dati dei tipi di carattere: combinando i tipi di carattere in un singolo file, i dati comuni possono essere de duplicate. Per questo motivo, un tipo di carattere o un riferimento al viso del tipo di carattere deve fare riferimento non solo a un file del tipo di carattere (o a un'origine dati equivalente), ma deve anche specificare un indice del tipo di carattere all'interno di tale file, per il caso generale in cui il file può essere un file di raccolta. 

Per i tipi di carattere usati sul Web, i dati dei tipi di carattere vengono spesso compressi in determinati formati di contenitore, WOFF o WOFF2, che forniscono una certa compressione dei dati del tipo di carattere e un certo livello di protezione dalla pirateria e dalla violazione delle licenze per i tipi di carattere. Dal punto di vista funzionale, un file WOFF o WOFF2 equivale a un tipo di carattere OpenType o a un file di raccolta di tipi di carattere, ma i dati vengono codificati in un formato diverso che richiede la decompressione prima di poter essere usati. 

Alcune DIRECTWRITE possono gestire singoli visi dei caratteri, mentre altre API possono gestire file che potrebbero includere file della raccolta OpenType che contengono più visi. Analogamente, alcune API gestiscono solo dati non elaborati in formato OpenType, mentre altre API possono gestire i formati di contenitore packed, WOFF e WOFF2. Questi dettagli sono disponibili nella discussione seguente. 

## <a name="font-sets-and-font-collections"></a>Set di caratteri e raccolte di tipi di carattere

Alcune applicazioni possono essere implementate per lavorare con i tipi di carattere usando [**l'interfaccia IDWriteFontCollection.**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) Esiste una corrispondenza diretta tra una raccolta di caratteri e un set di caratteri. Ognuno può contenere gli stessi tipi di carattere, ma presentarli con un'organizzazione diversa. Da qualsiasi raccolta di tipi di carattere è possibile ottenere un set di caratteri corrispondente e viceversa.

Quando si usano diversi tipi di carattere personalizzati, è più semplice usare un'interfaccia del generatore di set di caratteri per creare un set di tipi di carattere personalizzato e quindi ottenere una raccolta di tipi di carattere dopo la creazione del set di caratteri. Il processo per la creazione di un set di caratteri personalizzato verrà descritto in dettaglio di seguito. Per ottenere [**un'interfaccia IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) da un set di tipi di carattere, viene usato il [**metodo IDWriteFactory3::CreateFontCollectionFromFontSet.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-createfontcollectionfromfontset)

Se l'app ha un oggetto raccolta e deve ottenere un set di caratteri corrispondente, è possibile usare il metodo [**IDWriteFontCollection1::GetFontSet.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontcollection1-getfontset) 

## <a name="common-scenarios"></a>Scenari comuni

Questa sezione descrive alcuni degli scenari più comuni che coinvolgono set di caratteri personalizzati:

-   Creazione di un set di caratteri personalizzato usando tipi di carattere arbitrari nei percorsi nell'area file system.
-   Creazione di un set di caratteri personalizzato usando tipi di carattere noti (ad esempio in bundle con l'app) archiviati nel set di caratteri file system.
-   Creazione di un set di caratteri personalizzato usando tipi di carattere remoti noti sul Web.
-   Creazione di un set di caratteri personalizzato usando i dati del tipo di carattere caricati in memoria.

Le implementazioni complete per questi scenari sono disponibili nell'esempio DirectWrite [set di](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)caratteri personalizzati . Questo esempio illustra anche uno scenario più avanzato per la gestione dei dati dei tipi di carattere in formato contenitore WOFF o WOFF2, che verrà illustrato di seguito. 

### <a name="creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system"></a>Creazione di un set di caratteri usando tipi di carattere arbitrari nel file system

Quando si gestisce un set arbitrario di file di tipi di carattere nell'archiviazione locale, il metodo [**IDWriteFontSetBuilder1::AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) è utile perché, in una singola chiamata, può gestire tutti i visi del tipo di carattere all'interno di un file di raccolta di caratteri OpenType, nonché tutte le istanze per un tipo di carattere variabile OpenType. Questa opzione è disponibile nel Windows 10 Creators Update (build di anteprima 15021 o successiva) ed è consigliabile quando disponibile. 

Per usare questo metodo, usare il processo seguente.

<dl> 1.Per iniziare, creare <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">l'interfaccia IDWriteFactory5:</a> 


```C++
IDWriteFactory5* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
  DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



   
2. Usare la factory per ottenere <a href=""></a> [**l'interfaccia IDWriteFontSetBuilder1:**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) 


```C++
IDWriteFontSetBuilder1* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
}  
                
```



  
3. Per ogni file di tipo di carattere nel file system, creare un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) che faccia riferimento a esso: 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



   
4. Aggiungere [**l'oggetto IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) al generatore di set di caratteri usando il [**metodo AddFontFile:**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) 


```C++
hr = pFontSetBuilder->AddFontFile(pFontFile); 
```

Se il percorso del file specificato nella chiamata a [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) fa riferimento a un elemento diverso da un file OpenType supportato, la chiamata ad [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) restituirà un errore DWRITE \_ E \_ FILEFORMAT.

5. Dopo aver aggiunto tutti i file al generatore del set di caratteri, è possibile creare il set di caratteri personalizzato: 


```C++
IDWriteFontSet* pFontSet; 
hr = pFontSetBuilder->CreateFontSet(&pFontSet); 
```



   
</dl>

Se l'app deve essere eseguita in Windows 10 precedenti alla Windows 10 Creators Update, il metodo AddFontFile non sarà disponibile. La disponibilità può essere rilevata creando [**un'interfaccia IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) e quindi usando QueryInterface per provare a ottenere un'interfaccia [**IDWriteFactory5:**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) se l'operazione ha esito positivo, saranno disponibili anche l'interfaccia [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) e il metodo [**AddFontFile.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile)

Se il metodo AddFontFile non è disponibile, è necessario usare il metodo [**IDWriteFontSetBuilder::AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) per aggiungere singoli visi del tipo di carattere. Per consentire file OpenType Font Collection contenenti più visi, è possibile usare il metodo [**IDWriteFontFile::Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) per determinare il numero di visi contenuti nel file. Il processo è il seguente.

<dl> 1.Per iniziare, creare <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">l'interfaccia IDWriteFactory3:</a> 


```C++
IDWriteFactory3* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



  
2. Usare la factory per ottenere [**l'interfaccia IDWriteFontSetBuilder:**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) 


```C++
IDWriteFontSetBuilder* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
} 
```



  
3. Per ogni file di tipo di carattere, creare [**un idWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile), come illustrato in precedenza: 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



Anziché aggiungere il file direttamente al generatore del set di caratteri, è necessario determinare il numero di visi e creare singoli [**oggetti IDWriteFontFaceReference.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)   
4. Usare il [**metodo Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) per ottenere il numero di visi nel file. 


```C++
BOOL isSupported; 
DWRITE_FONT_FILE_TYPE fileType; 
UINT32 numberOfFonts; 
hr = pFontFile->Analyze(&isSupported, &fileType, /* face type */ nullptr, &numberOfFonts); 
```



Il [**metodo Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) imposta anche i valori per i parametri isSupported e fileType. Se il file non è un formato supportato, isSupported sarà FALSE e sarà possibile eseguire l'azione appropriata, ad esempio ignorare il file.   
5. Eseguire un ciclo sul numero di tipi di carattere impostati nel parametro numberOfFonts. All'interno del ciclo creare un [**elemento IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) per ogni coppia file/indice e aggiungerlo al generatore del set di caratteri. 


```C++
for (uint32_t fontIndex = 0; fontIndex < numberOfFonts; fontIndex++) 
{ 
  IDWriteFontFaceReference* pFontFaceReference;
  hr = pDWriteFactory->CreateFontFaceReference(pFontFile, fontIndex, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);

  if (SUCCEEDED(hr))
  {
    hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference);
  }
} 
```



  
6. Dopo aver aggiunto tutti i visi al generatore del set di caratteri, creare il set di caratteri personalizzato, come illustrato in precedenza.  
</dl>

Un'app può essere progettata in modo da usare il metodo [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) preferito durante l'esecuzione nel Windows 10 Creators Update, ma eseguire il fall back per usare il metodo [**AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) quando è in esecuzione in versioni Windows 10 precedenti. Testare la disponibilità [**dell'interfaccia IDWriteFactory5,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) come descritto in precedenza, e quindi eseguire il branch di conseguenza. Questo approccio è illustrato nell'esempio [DirectWrite set di caratteri personalizzati](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). 

### <a name="creating-a-font-set-using-known-fonts-in-the-local-file-system"></a>Creazione di un set di tipi di carattere usando tipi di carattere noti nel file system

Come accennato in precedenza, ogni riferimento al viso del tipo di carattere in un set di caratteri è associato a determinate proprietà in formato informativo, ad esempio il nome della famiglia e lo spessore del carattere. Quando i tipi di carattere personalizzati vengono aggiunti a un generatore di set di caratteri usando le chiamate API elencate in precedenza, queste proprietà in formato informativo vengono ottenute direttamente dai dati effettivi del tipo di carattere, che vengono letti quando viene aggiunto il tipo di carattere. In alcune situazioni, tuttavia, se un'app ha un'altra origine di informazioni su un tipo di carattere, potrebbe voler fornire i propri valori personalizzati per queste proprietà. 

Ad esempio, si supponga che un'app in bundle alcuni tipi di carattere usati per presentare particolari elementi dell'interfaccia utente all'interno dell'app. A volte, ad esempio con una nuova versione dell'app, potrebbe essere necessario modificare i tipi di carattere specifici che l'app usa per questi elementi. Se l'app ha riferimenti codificati ai tipi di carattere specifici, la sostituzione di un tipo di carattere con un altro richiede la modifica di ognuno di questi riferimenti. Se invece l'app usa proprietà personalizzate per assegnare alias funzionali in base al tipo di elemento o di testo sottoposto a rendering, esegue il mapping di ogni alias a un tipo di carattere specifico in un'unica posizione e quindi usa gli alias in tutti i contesti in cui i tipi di carattere vengono creati e manipolati, quindi la sostituzione di un tipo di carattere con un altro richiede solo la modifica della posizione in cui viene eseguito il mapping dell'alias a un tipo di carattere specifico. 

I valori personalizzati per le proprietà in formato informativo possono essere assegnati quando viene chiamato il metodo [**IDWriteFontSetBuilder::AddFontFaceReference.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) Il metodo per eseguire questa operazione è il seguente. può essere usato in qualsiasi Windows 10 versione. 

Come illustrato in precedenza, iniziare ottenendo le [**interfacce IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) e [**IDWriteFontSet.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) Per ogni viso del tipo di carattere personalizzato da aggiungere, creare un [**oggetto IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference), come illustrato in precedenza. Prima che venga aggiunto al generatore di set di caratteri (all'interno del ciclo nel passaggio 5, illustrato in precedenza), tuttavia, l'app definisce i valori delle proprietà personalizzate da usare. 

Un set di valori di proprietà personalizzati viene definito usando una matrice di [**strutture DWRITE \_ FONT \_ PROPERTY.**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) Ognuna di queste identifica una determinata proprietà dall'enumerazione [**DWRITE \_ FONT PROPERTY \_ \_ ID**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) e il valore della proprietà corrispondente da utilizzare.  

Si noti che tutti i valori delle proprietà vengono assegnati come stringhe. Se in un secondo momento possono essere visualizzati agli utenti, è possibile impostare valori alternativi per una determinata proprietà per lingue diverse, ma non è obbligatorio. Si noti anche che se l'app imposta valori di proprietà personalizzati, solo i valori specificati verranno usati all'interno del set di caratteri. DirectWrite non deriverà alcun valore direttamente dal tipo di carattere per le proprietà in formato informativo usate in un set di caratteri. 

Nell'esempio seguente vengono definiti valori personalizzati per tre proprietà in formato informativo: nome della famiglia, nome completo e spessore del carattere. 


```C++
DWRITE_FONT_PROPERTY props[] = 
{ 
  { DWRITE_FONT_PROPERTY_ID_FAMILY_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_FULL_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_WEIGHT, L"400", nullptr } 
}; 
               
            
```



Dopo aver definito la matrice desiderata di valori di proprietà per un tipo di carattere, effettuare una chiamata a AddFontFaceRefence, passando la matrice di proprietà e il riferimento al viso del tipo di carattere. 


```C++
hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference, props, ARRAYSIZE(props)); 
```



 

Dopo aver aggiunto tutti i visi del tipo di carattere personalizzati al generatore del set di caratteri, insieme alle relative proprietà personalizzate, creare il set di caratteri personalizzato, come illustrato in precedenza. 

### <a name="creating-a-custom-font-set-using-known-remote-fonts-on-the-web"></a>Creazione di un set di caratteri personalizzato usando tipi di carattere remoti noti sul Web

Le proprietà personalizzate sono importanti per l'uso dei tipi di carattere remoti. Ogni riferimento al tipo di carattere deve avere alcune proprietà in formato informativo per caratterizzare il tipo di carattere e distinguerlo dagli altri tipi di carattere. Poiché i dati del tipo di carattere per i tipi di carattere remoti non sono locali, DirectWrite le proprietà non possono derivare direttamente dai dati del tipo di carattere. Di conseguenza, le proprietà devono essere fornite in modo esplicito quando si aggiunge un tipo di carattere remoto al generatore del set di caratteri.

La sequenza di chiamate API per l'aggiunta di tipi di carattere remoti a un set di tipi di carattere è simile alla sequenza descritta per lo scenario precedente. Poiché i dati del tipo di carattere sono remoti, tuttavia, le operazioni di lettura dei dati effettivi del tipo di carattere saranno diverse da quelle eseguite con i file nell'archiviazione locale. In questo caso, è stata aggiunta una nuova interfaccia di livello inferiore, [**IDWriteRemoteFontFileLoader,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader)nel Windows 10 Creators Update. 

Per usare il caricatore di file del tipo di carattere remoto, è necessario prima registrarlo con una DirectWrite factory. Il caricatore dovrà essere mantenuto dall'app per tutto il tempo in cui vengono usati i tipi di carattere associati. Quando i tipi di carattere non sono più in uso e a un certo punto prima dell'eliminazione della factory, è necessario annullare la registrazione del caricatore. Questa operazione può essere eseguita nel distruttore per la classe proprietaria dell'oggetto caricatore. Questi passaggi verranno illustrati di seguito. 

Il metodo per la creazione di un set di caratteri personalizzato con tipi di carattere remoti è il seguente. questa operazione richiede l'Windows 10 Creators Update.  

<dl> 1. Creare un'interfaccia IDWriteFactory5, come illustrato in precedenza.   
2. Creare <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">un'interfaccia IDWriteFontSetBuilder,</a> come illustrato in precedenza.   
3.Usare la factory per ottenere un <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader">oggetto IDWriteRemoteFontFileLoader.</a> 


```C++
IDWriteRemoteFontFileLoader* pRemoteFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateHttpFontFileLoader( 
        /* referrerURL */ nullptr, 
        /* extraHeaders */ nullptr, 
        &pRemoteFontFileLoader 
    ); 
} 
```



Viene restituita un'implementazione fornita dal sistema dell'interfaccia del caricatore di file dei tipi di carattere remota in grado di gestire le interazioni HTTP per scaricare i dati dei tipi di carattere per conto dell'app. Un URL referrer o intestazioni aggiuntive possono essere specificate se richiesto dal servizio di tipi di carattere o dai servizi che sono l'origine per i tipi di carattere.    

> [!IMPORTANT]
> Nota sulla sicurezza: quando si tenta di recuperare un tipo di carattere remoto, un utente malintenzionato potrebbe eseguire lo spoofing del server previsto che verrà chiamato. In tal caso, gli URL di destinazione e di riferimento e i dettagli dell'intestazione verranno divulgati all'utente malintenzionato. Gli sviluppatori di app sono responsabili della mitigazione di questo rischio. È consigliabile usare il protocollo HTTPS anziché HTTP. 

 

È possibile usare un singolo caricatore di file di tipi di carattere remoto per più tipi di carattere, anche se è possibile usare caricatori diversi se i tipi di carattere vengono ottenuti da più servizi con requisiti diversi per l'URL del referrer o intestazioni aggiuntive.   
4. Registrare il caricatore di file del tipo di carattere remoto con la factory. 


```C++
 if (SUCCEEDED(hr)) 
 { 
     hr = pDWriteFactory->RegisterFontFileLoader(pRemoteFontFileLoader); 
 } 
```



A questo punto, i passaggi per la creazione del set di caratteri personalizzato sono simili a quelli descritti per i file di tipi di carattere locali noti, con due importanti eccezioni. In primo luogo, [**l'oggetto IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) viene creato usando l'interfaccia del caricatore di file del tipo di carattere remoto anziché la factory. In secondo momento, non è possibile usare il metodo Analyze perché i dati del tipo di carattere non sono locali. Al contrario, l'app deve sapere se il file del tipo di carattere remoto è un file OpenType Font Collection e, in tal caso, deve sapere quale dei tipi di carattere all'interno della raccolta userà e l'indice per ognuno. Di conseguenza, i passaggi rimanenti sono i seguenti.   
5. Per ogni file di tipo di carattere remoto, usare l'interfaccia del caricatore del file del tipo di carattere remoto per creare un [**oggetto IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile), specificando l'URL necessario per accedere al file del tipo di carattere. 


```C++
 IDWriteFontFile* pFontFile; 
 hr = pRemoteFontFileLoader->CreateFontFileReferenceFromUrl( 
     pDWriteFactory, 
     /* baseUrl */ L"https://github.com/", 
     /* fontFileUrl */ L"winjs/winjs/blob/master/src/fonts/Symbols.ttf?raw=true", 
     &pFontFile 
 ); 
```



Si noti che l'URL completo può essere specificato nel parametro fontFileUrl oppure può essere suddiviso in parti di base e relative. Se viene specificato un URL di base, la concatenazione dei valori baseUrl e fontFileUrl deve fornire l'URL completo, DirectWrite non fornirà alcun delimitatore aggiuntivo.  

> [!IMPORTANT]
> Nota sulla sicurezza/sulle prestazioni: quando si tenta di recuperare un tipo di carattere remoto, non è garantito che Windows riceverà una risposta dal server. In alcuni casi, un server può rispondere con un errore di file non trovato per un URL relativo non valido, ma smettere di rispondere se riceve più richieste non valide. Se il server non risponde, Windows timeout, anche se l'avvio di più recuperi può richiedere alcuni minuti. È consigliabile fare tutto il possibile per assicurarsi che gli URL siano validi quando vengono effettuate chiamate. 

 

Si noti anche che l'URL può puntare a un file di tipo di carattere OpenType non elaborato (con estensione ttf, otf, ttc, otc), ma può anche puntare ai tipi di carattere in un file contenitore WOFF o WOFF2. Se si fa riferimento a un file WOFF o WOFF2, l'implementazione DirectWrite del caricatore del file del tipo di carattere remoto decomprime automaticamente i dati del tipo di carattere dal file contenitore.   
6. Per ogni indice del viso del tipo di carattere all'interno del file del tipo di carattere remoto da usare, creare un [**oggetto IDWriteFontFaceReference.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) 


```C++
 IDWriteFontFaceReference* pFontFaceReference; 
 hr = pDWriteFactory->CreateFontFaceReference(pFontFile, /* faceIndex */ 0, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);
```



  
7. Definire proprietà personalizzate per il tipo di carattere, come illustrato in precedenza.   
8. Aggiungere il riferimento al viso del tipo di carattere insieme alle proprietà personalizzate al generatore del set di caratteri, come illustrato in precedenza.   
9. Dopo aver aggiunto tutti i tipi di carattere al generatore del set di caratteri, creare il set di tipi di carattere, come illustrato in precedenza.   
10. A un certo punto, quando i tipi di carattere remoti non verranno più usati, annullare la registrazione del caricatore del file dei tipi di carattere remoto. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pRemoteFontFileLoader); 
```



  
</dl>

Dopo aver creato un set di tipi di carattere personalizzato con tipi di carattere remoti personalizzati, il set di caratteri contiene riferimenti e proprietà in formato informativo per i tipi di carattere remoti, ma i dati effettivi sono ancora remoti. DirectWrite il supporto per i tipi di carattere remoti consente di mantenere un riferimento al tipo di carattere nel set di caratteri e di selezionare un tipo di carattere per l'uso nel layout e nel rendering, ma che i dati effettivi non vengono scaricati fino a quando non è effettivamente necessario usarlo, ad esempio quando verrà eseguito il layout di testo.  

Un'app può adottare un approccio in anticipo richiedendo al DirectWrite di scaricare i dati del tipo di carattere e quindi attendendo la conferma di un download riuscito prima dell'avvio di qualsiasi elaborazione con il tipo di carattere. Tuttavia, un download di rete implica una certa latenza di durata imprevedibile e anche il successo è incerto. Per questo motivo, in genere è meglio adottare un approccio diverso, consentendo di eseguire inizialmente layout e rendering usando tipi di carattere alternativi o di fallback già locali, richiedendo il download del tipo di carattere remoto desiderato in parallelo e quindi aggiornando i risultati dopo aver scaricato il tipo di carattere desiderato. 

Per richiedere che l'intero tipo di carattere venga scaricato prima di essere usato, è possibile usare il metodo [**IDWriteFontFaceReference::EnqueueFontDownloadRequest.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuefontdownloadrequest) Se il tipo di carattere è molto grande, potrebbe essere necessaria solo una parte dei dati per l'elaborazione di stringhe specifiche. DirectWrite fornisce metodi aggiuntivi che possono essere usati per richiedere parti dei dati del tipo di carattere necessari per un particolare contenuto, [**EnqueueCharacterDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuecharacterdownloadrequest) e [**EnqueueGlyphDownloadRequest.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueueglyphdownloadrequest)  

Si supponga che l'approccio da prendere nell'app sia quello di consentire l'elaborazione iniziale usando tipi di carattere locali, alternativi o di fallback. Il metodo IDWriteFontFallback::[**MapCharacters**](idwritefontfallback-mapcharacters.md) può essere usato per identificare i tipi di carattere di fallback locali e accoderà automaticamente anche una richiesta di download del tipo di carattere preferito. Inoltre, se viene usato [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e parte o tutto il testo nel layout viene formattato usando un riferimento al tipo di carattere remoto, DirectWrite userà automaticamente il metodo **MapCharacters** per ottenere i tipi di carattere di fallback locali e per accodare una richiesta per scaricare i dati del tipo di carattere remoto. 

DirectWrite gestisce una coda di download dei tipi di carattere per ogni factory e le richieste effettuate usando i metodi indicati in precedenza vengono aggiunte a tale coda. La coda di download dei tipi di carattere può essere ottenuta usando il [**metodo IDWriteFactory3::GetFontDownloadQueue.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getfontdownloadqueue) 

Se viene effettuata una richiesta di download ma i dati del tipo di carattere sono già locali, verrà restituita una richiesta no-op: non verrà aggiunto alcun elemento alla coda di download. Un'app può controllare se la coda è vuota o se sono presenti richieste di download in sospeso chiamando il [**metodo IDWriteFontDownloadQueue::IsEmpty.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-isempty) 

Dopo l'aggiunta delle richieste di tipo di carattere remoto alla coda, è necessario inizializzare il processo di download. Quando i tipi di carattere remoti vengono usati in [**IDWriteTextLayout,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)il download verrà avviato automaticamente quando l'app chiama i metodi **IDWriteTextLayout** che forzano operazioni di layout o rendering, ad esempio i metodi GetLineMetrics o Draw. In altri scenari, l'app deve avviare il download direttamente chiamando [**IDWriteFontDownloadQueue::BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload).  

Al termine di un download, l'app dovrà eseguire le azioni appropriate, ovvero procedere con le operazioni in sospeso o ripetere le operazioni eseguite inizialmente con i tipi di carattere di fallback. Se viene DirectWrite layout di testo del controllo, è possibile usare [**IDWriteTextLayout3::InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) per cancellare i risultati temporanei calcolati usando i tipi di carattere di fallback. Per ricevere una notifica all'app al termine del processo di download e per eseguire le azioni appropriate, l'app deve fornire un'implementazione dell'interfaccia [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) e passarla alla chiamata BeginDownload. 

> [!IMPORTANT]
> Nota sulla sicurezza/sulle prestazioni: quando si tenta di recuperare un tipo di carattere remoto, non è garantito che Windows riceverà una risposta dal server. Se il server non risponde, Windows timeout, anche se questa operazione può richiedere alcuni minuti se più tipi di carattere remoti vengono recuperati ma non riescono. La chiamata BeginDownload verrà restituita immediatamente. Le app non devono bloccare l'interfaccia utente durante l'attesa della [**chiamata a IDWriteFontDownloadListener::D ownloadCompleted.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadlistener-downloadcompleted) 

 

Le implementazioni di esempio di queste interazioni con la coda di download dei tipi di carattere di DirectWrite e l'interfaccia [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) sono disponibili nell'esempio di set di caratteri personalizzati [di DirectWrite](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)e anche nell'esempio di tipi di carattere [scaricabili di DirectWrite.](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont) 

### <a name="creating-a-custom-font-set-using-font-data-loaded-into-memory"></a>Creazione di un set di tipi di carattere personalizzato usando i dati dei tipi di carattere caricati in memoria

Così come le operazioni di basso livello per la lettura dei dati da un file del tipo di carattere sono diverse per i file su un disco locale rispetto ai file remoti sul Web, lo stesso vale anche per i dati dei tipi di carattere caricati in un buffer di memoria. È stata aggiunta una nuova interfaccia di basso livello per la gestione dei dati dei tipi di carattere in memoria nel Windows 10 Creators Update, [**IDWriteInMemoryFontFileLoader.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) 

Come per un caricatore di file di tipi di carattere remoto, un caricatore di file dei tipi di carattere in memoria deve prima essere registrato con una factory DirectWrite factory. Il caricatore dovrà essere mantenuto dall'app per tutto il tempo in cui vengono usati i tipi di carattere associati. Quando i tipi di carattere non sono più in uso e a un certo punto prima dell'eliminazione della factory, è necessario annullare la registrazione del caricatore. Questa operazione può essere eseguita nel distruttore per la classe proprietaria dell'oggetto caricatore. Questi passaggi verranno illustrati di seguito. 

Se l'app dispone di informazioni separate sui visi dei tipi di carattere rappresentati dai dati, può aggiungere singoli riferimenti ai visi dei caratteri a un generatore di set di caratteri con le proprietà personalizzate specificate. Poiché i dati del tipo di carattere si trova nella memoria locale, tuttavia, questa operazione non è necessaria. DirectWrite sarà in grado di leggere i dati direttamente per derivare i valori delle proprietà. 

DirectWrite presuppone che i dati del tipo di carattere siano in formato OpenType non elaborato, equivalente a un file OpenType (con estensione ttf, otf, ttc, otc), ma in memoria anziché su disco. I dati non possono essere in formato contenitore WOFF o WOFF2. I dati possono rappresentare una raccolta di tipi di carattere OpenType. Se non vengono usate proprietà personalizzate, è possibile usare il metodo [**IDWriteFontSetBuilder1::AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) per aggiungere tutti i visi dei tipi di carattere nei dati in una singola chiamata. 

Una considerazione importante per lo scenario in memoria è la durata dei dati. Se un puntatore al buffer viene fornito al DirectWrite senza una chiara indicazione che è presente un proprietario, DirectWrite crea una copia dei dati in un nuovo buffer di memoria di cui sarà proprietario. Per evitare la copia dei dati e l'allocazione di memoria aggiuntiva, l'app può passare un oggetto proprietario dei dati che implementa IUnknown e che possiede il buffer di memoria contenente i dati del tipo di carattere. Implementando questa interfaccia, DirectWrite possibile aggiungere al conteggio dei riferimenti dell'oggetto, garantendo in tal modo la durata dei dati di proprietà. 

Il metodo per la creazione di un set di caratteri personalizzato usando i dati dei tipi di carattere in memoria è il seguente: a questo scopo è necessario Windows 10 Creators Update. Si presuppone un oggetto proprietario dei dati implementato dall'app, che implementa IUnknown e dispone anche di metodi che restituiscono un puntatore al buffer di memoria e le dimensioni del buffer. 

<dl> 1. Creare un'interfaccia IDWriteFactory5, come illustrato in precedenza.  
2. Creare [**un'interfaccia IDWriteFontSetBuilder1,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) come illustrato in precedenza.  
3. Usare la factory per ottenere un oggetto IDWriteInMemoryFontFileLoader. 


```C++
 IDWriteInMemoryFontFileLoader* pInMemoryFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateInMemoryFontFileLoader(&pInMemoryFontFileLoader); 
}
```



Viene restituita un'implementazione fornita dal sistema dell'interfaccia del caricatore di file dei tipi di carattere in memoria.   
4. Registrare il caricatore di file dei tipi di carattere in memoria con la factory. 


```C++
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->RegisterFontFileLoader(pInMemoryFontFileLoader); 
}
```



   
5. Per ogni file di tipo di carattere in memoria, usare il caricatore del file dei tipi di carattere in memoria per creare un [**oggetto IDWriteFontFile.**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) 


```C++
IDWriteFontFile* pFontFile; 
hr = pInMemoryFontFileLoader->CreateInMemoryFontFileReference( 
    pDWriteFactory, 
    pFontDataOwner->fontData /* returns void* */, 
    pFontDataOwner->fontDataSize /* returns UINT32 */, 
    pFontDataOwner /* ownerObject, owns the memory with font data and implements IUknown */, 
    &pFontFile 
); 
```



   
6. Aggiungere [**l'oggetto IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) al generatore di set di tipi di carattere usando [**il metodo AddFontFile,**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) come illustrato in precedenza.  Se è necessario, l'app può invece creare singoli oggetti [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) in base a **IDWriteFontFile,** definire facoltativamente proprietà personalizzate per ogni riferimento al viso del tipo di carattere e quindi aggiungere il riferimento al tipo di carattere con proprietà personalizzate al set di caratteri usando il metodo [**AddFontFaceReference,**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) come illustrato in precedenza.   
7. Dopo aver aggiunto tutti i tipi di carattere al generatore del set di caratteri, creare il set di caratteri personalizzato, come illustrato in precedenza.   
8. A un certo punto, quando i tipi di carattere in memoria non verranno più usati, annullare la registrazione del caricatore di file dei tipi di carattere in memoria. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pInMemoryFontFileLoader);
```



  
</dl>

 

## <a name="advanced-scenarios"></a>Scenari avanzati

Alcune app possono avere requisiti speciali che richiedono un'elaborazione più avanzata rispetto a quanto descritto in precedenza. 

### <a name="combining-font-sets"></a>Combinazione di set di caratteri

Alcune app potrebbero dover creare un set di caratteri che include una combinazione di elementi di altri set di caratteri. Ad esempio, un'app potrebbe voler creare un set di tipi di carattere che combina tutti i tipi di carattere installati nel sistema con una selezione di tipi di carattere personalizzati oppure combina i tipi di carattere installati corrispondenti a determinati criteri con altri tipi di carattere. DirectWrite dispone di API per supportare la manipolazione e la combinazione di set di caratteri. 

Per combinare due o più set di tipi di carattere, il metodo [**IDWriteFontSetBuilder::AddFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontset) aggiunge tutti i tipi di carattere nel set di caratteri specificato da aggiungere a un generatore di set di tipi di carattere in una singola chiamata. Se nel nuovo set di tipi di carattere sono presenti solo determinati tipi di carattere di un set di caratteri esistente, è possibile usare il metodo [**IDWriteFontSet::GetMatchingFonts**](idwritefontset-getmatchingfonts-overload.md) per derivare un nuovo oggetto set di tipi di carattere filtrato in modo da includere solo i tipi di carattere corrispondenti alle proprietà specificate. Questi metodi consentono di creare facilmente un set di caratteri personalizzato combinando i tipi di carattere da due o più set di caratteri esistenti 

### <a name="using-local-woff-or-woff2-font-data"></a>Uso dei dati del tipo di carattere WOFF o WOFF2 locali

Se un'app include file di tipi di carattere nel file system locale o in un buffer di memoria, ma usano i formati di contenitore WOFF o WOFF2, DirectWrite (Windows 10 Creator Update o versioni successive) fornisce un metodo per decomprimere il formato del [**contenitore, IDWriteFactory5::UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile), che restituisce [**idWriteFontFileStream.**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 

Tuttavia, l'app avrà bisogno di un modo per ottenere [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) in un oggetto caricatore di file di tipi di carattere. Un modo per eseguire questa operazione è creare un'implementazione [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) personalizzata che esegue il wrapping del flusso. Come per gli altri caricatori di file dei tipi di carattere, questa operazione deve essere registrata prima dell'uso e annullata prima che la factory eseva dall'ambito.  

Se il caricatore personalizzato verrà usato anche con file di tipi di carattere non elaborati (non di tipo pack), l'app dovrà anche fornire un'implementazione personalizzata dell'interfaccia [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) per la gestione di tali file. Esistono tuttavia modi più semplici per usare le API descritte in precedenza per la gestione dei file dei tipi di carattere non elaborati. È possibile evitare la necessità di un'implementazione del flusso personalizzata usando percorsi di codice separati per i file dei tipi di carattere di tipo pack rispetto ai file dei tipi di carattere non elaborati. 

Dopo la creazione di un oggetto caricatore di file di tipi di carattere personalizzato, i dati del file del tipo di carattere di cui è stato creato il pacchetto vengono aggiunti al caricatore in base alle specifiche dell'app. Il caricatore può gestire più file di tipi di carattere, ognuno dei quali viene identificato usando una chiave definita dall'app opaca per DirectWrite. Dopo l'aggiunta di un file di tipo di carattere di tipo pack al caricatore, viene usato il metodo [**IDWriteFactory::CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) per ottenere un [**idWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) basato su tale caricatore per i dati del tipo di carattere identificati da una chiave specificata.  

La decompressione effettiva dei dati del tipo di carattere può essere eseguita quando i tipi di carattere vengono aggiunti al caricatore, ma può essere gestita anche nel metodo [**IDWriteFontFileLoader::CreateStreamFromKey,**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) che DirectWrite chiamerà quando deve leggere i dati del tipo di carattere per la prima volta. 

Dopo aver creato un oggetto IDWriteFontFile, i passaggi rimanenti per aggiungere i tipi di carattere a un set di tipi di carattere personalizzato saranno quelli descritti in precedenza. 

Un'implementazione che usa questo approccio è illustrata [nell'esempio DirectWrite set di caratteri personalizzati](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). 

### <a name="using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation"></a>Uso DirectWrite dei tipi di carattere remoti con l'implementazione di rete di basso livello personalizzata

I meccanismi DirectWrite per la gestione dei tipi di carattere remoti possono essere suddivisi in meccanismi di livello superiore, ovvero set di caratteri che includono riferimenti ai visi dei tipi di carattere remoti, controllo della posizione dei dati dei tipi di carattere e gestione della coda per le richieste di download dei tipi di carattere, e meccanismi di livello inferiore che gestiscono il download effettivo. Alcune app potrebbero voler usare i meccanismi dei tipi di carattere remoti di livello superiore, ma richiedono anche interazioni di rete personalizzate, ad esempio la comunicazione con i server tramite protocolli diversi da HTTP. 

In questo caso, un'app dovrà creare un'implementazione personalizzata dell'interfaccia [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) che interagisce con altre interfacce di livello inferiore nei modi richiesti. L'app dovrà anche fornire implementazioni personalizzate di queste interfacce di livello inferiore: [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream)e [**IDWriteAsyncResult.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) Queste tre interfacce hanno metodi di callback che DirectWrite chiamare durante le operazioni di download. 

Quando viene chiamato [**IDWriteFontDownloadQueue::BeginDownload,**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload) DirectWrite esegue query al caricatore di file dei tipi di carattere remoto sulla localizzazione dei dati e richiede il flusso remoto. Se i dati non sono locali, chiamerà il metodo BeginDownload del flusso. L'implementazione del flusso non deve bloccarsi su tale chiamata, ma deve restituire immediatamente, passando un [**oggetto IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) che fornisce l'handle di attesa che DirectWrite userà per attendere l'operazione di download asincrona. L'implementazione del flusso personalizzato è responsabile della gestione della comunicazione remota. Quando si è verificato l'evento di completamento, DirectWrite [**idWriteAsyncResult::GetResult**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteasyncresult-getresult) per determinare il risultato dell'operazione. Se il risultato ha esito positivo, è previsto che le chiamate ReadFragment successive al flusso per gli intervalli scaricati avranno esito positivo. 

> [!IMPORTANT]
> Nota sulla sicurezza/sulle prestazioni: quando si tenta di recuperare un tipo di carattere remoto, esiste in generale la possibilità che un utente malintenzionato possa effettuare lo spoofing del server previsto chiamato o che il server non risponda. Se si implementano interazioni di rete personalizzate, è possibile avere un maggiore controllo sulle mitigazioni rispetto a quando si gestiscono server di terze parti. Tuttavia, è necessario prendere in considerazione le soluzioni appropriate per evitare la divulgazione di informazioni o la negazione del servizio. Sono consigliati protocolli sicuri come HTTPS. È anche consigliabile compilare in un timeout in modo che l'handle di evento restituito DirectWrite non sia impostato. 

 

### <a name="supporting-scenarios-on-earlier-windows-versions"></a>Scenari di supporto nelle versioni Windows precedenti

Gli scenari descritti possono essere supportati in DirectWrite nelle versioni precedenti di Windows, ma richiederebbero un'implementazione molto più personalizzata da parte dell'app usando le API più limitate disponibili prima di Windows 10. Per altre informazioni, vedere [Raccolte di caratteri personalizzati (Windows 7/8).](custom-font-collections.md)

 

 