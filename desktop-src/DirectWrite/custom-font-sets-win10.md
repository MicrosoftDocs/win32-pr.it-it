---
title: Set di caratteri personalizzati
description: Questo argomento descrive i vari modi in cui è possibile usare i tipi di carattere personalizzati nell'app.
ms.assetid: 50842838-d150-df9a-f1b7-67ce5ea2bc80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a79f1ccfcb1dadd355c5f582417aacb5041ecf8b
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "104399912"
---
# <a name="custom-font-sets"></a>Set di caratteri personalizzati

Questo argomento descrive i vari modi in cui è possibile usare i tipi di carattere personalizzati nell'app.

-   [Introduzione ](#introduction)
-   [Riepilogo delle API](#summary-of-apis)
-   [Concetti chiave](#key-concepts)
-   [Tipi di carattere e formati di file dei tipi di carattere](#fonts-and-font-file-formats)
-   [Set di caratteri e raccolte di tipi di carattere](#font-sets-and-font-collections)
-   [Scenari comuni](#common-scenarios)
    -   [Creazione di un set di caratteri utilizzando tipi di carattere arbitrari nell'file system locale](#creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system)
    -   [Creazione di un set di caratteri utilizzando i tipi di carattere noti nella file system locale](#creating-a-font-set-using-known-fonts-in-the-local-file-system)
    -   [Creazione di un set di caratteri personalizzato utilizzando caratteri remoti noti sul Web](#creating-a-custom-font-set-using-known-remote-fonts-on-the-web)
    -   [Creazione di un set di caratteri personalizzato usando i dati del tipo di carattere caricati in memoria](#creating-a-custom-font-set-using-font-data-loaded-into-memory)
-   [Scenari avanzati](#advanced-scenarios)
    -   [Combinazione di set di caratteri](#combining-font-sets)
    -   [Uso di dati di tipo carattere WOFF o WOFF2 locali ](#using-local-woff-or-woff2-font-data)
    -   [Uso di meccanismi di tipo carattere remoto DirectWrite con implementazione di rete di basso livello personalizzata ](#using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation)
    -   [Scenari di supporto nelle versioni precedenti di Windows ](#supporting-scenarios-on-earlier-windows-versions)

## <a name="introduction"></a>Introduzione

Nella maggior parte dei casi, le app utilizzano i tipi di carattere installati localmente nel sistema. DirectWrite consente di accedere a questi tipi di carattere usando i metodi [**IDWriteFactory3:: GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) o [**IDWriteFactory archiviata nei:: GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . In alcuni casi, le app potrebbero anche voler usare i tipi di carattere inclusi come parte di Windows 10, ma che non sono attualmente installati nel sistema corrente. È possibile accedere a questi tipi di carattere dal servizio Windows font usando il metodo **GetSystemFontSet** oppure chiamando [**IDWriteFactory3:: GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection) con includeDownloadableFonts impostato su true. 

In alcuni scenari di applicazione, tuttavia, le app devono usare i tipi di carattere che non sono installati nel sistema e non vengono forniti dal servizio del tipo di carattere di Windows. Di seguito sono riportati alcuni esempi di scenari di questo tipo:

-   I tipi di carattere vengono incorporati come risorse in un file binario dell'app.
-   I file del tipo di carattere sono aggregati in un pacchetto dell'app e archiviati su disco nella cartella di installazione dell'app.
-   L'app è uno strumento di sviluppo di tipi di carattere che deve caricare i file dei tipi di carattere specificati dall'utente. 
-   I tipi di carattere sono incorporati nei file di documento che possono essere visualizzati o modificati nell'app. 
-   L'app usa i tipi di carattere ottenuti da un servizio Web pubblico. 
-   L'app usa i dati del tipo di carattere trasmessi tramite un protocollo di rete privato. 

DirectWrite fornisce le API per l'utilizzo di tipi di carattere personalizzati in questi e in altri scenari simili. I dati del tipo di carattere personalizzati possono provenire da file nel file system locale; da origini remote basate sul cloud a cui si accede tramite HTTP; o da origini arbitrarie dopo che sono state caricate in un buffer di memoria. 

> [!Note]  
> Anche se DirectWrite ha fornito API per l'uso di tipi di carattere personalizzati a partire da Windows 7, le API più recenti sono state aggiunte in Windows 10 e di nuovo in Windows 10 Creators Update (versione di anteprima 15021 o successiva) che semplificano l'implementazione di diversi scenari citati. Questo argomento è incentrato sulle API disponibili nella finestra 10. Per le applicazioni che devono funzionare nelle versioni precedenti di Windows, vedere [raccolte di tipi di carattere personalizzati (Windows 7/8)](custom-font-collections.md). 

 

## <a name="summary-of-apis"></a>Riepilogo delle API

Questo argomento è incentrato sulle funzionalità fornite dalle API seguenti: 

-   Interfaccia [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
-   Interfaccia [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
-   Interfaccia [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) 
-   Interfaccia [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)
-   Interfaccia [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)
-   Metodo [**IDWriteFactory archiviata nei:: CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) 
-   Metodo [**IDWriteFactory archiviata nei:: CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) 
-   Metodi [**IDWriteFactory3:: CreateFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontresource-createfontfacereference) 
-   [**DWrite \_ Struttura della \_ proprietà font**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) 
-   [**DWrite \_ Enumerazione \_ \_ ID proprietà carattere**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) 
-   Interfaccia [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) 
-   Metodo [**IDWriteFactory archiviata nei:: RegisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader) 
-   Metodo [**IDWriteFactory archiviata nei:: UnregisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontfileloader) 
-   Metodo [**IDWriteFactory5:: CreateInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createinmemoryfontfileloader) 
-   Interfaccia [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) 
-   Metodo [**IDWriteFactory5:: CreateHttpFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createhttpfontfileloader) 
-   Interfaccia [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) 
-   Interfaccia [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) 
-   Interfaccia [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) 
-   Interfaccia [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 
-   Interfaccia [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) 
-   Interfaccia [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) 
-   Metodo [**IDWriteFactory5:: AnalyzeContainerType**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-analyzecontainertype) 
-   Metodo [**IDWriteFactory5:: UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile) 

 

## <a name="key-concepts"></a>Concetti chiave

Per comprendere le API DirectWrite per l'uso di tipi di carattere personalizzati, può essere utile comprendere il modello concettuale che sottende tali API. I concetti chiave verranno descritti qui. 

Quando DirectWrite esegue il layout o il rendering del testo effettivo, deve accedere ai dati dei tipi di carattere effettivi. Un oggetto del tipo di carattere contiene i dati del tipo di carattere effettivi che devono esistere nel sistema locale. Tuttavia, per altre operazioni, ad esempio per controllare la disponibilità di un particolare tipo di carattere o per presentare scelte di tipi di carattere a un utente, è sufficiente un riferimento a un particolare tipo di carattere, non i dati effettivi del tipo di carattere. In DirectWrite un oggetto di riferimento del tipo di carattere include solo le informazioni necessarie per individuare e creare un'istanza di un tipo di carattere. Poiché il riferimento al tipo di carattere non tiene i dati effettivi, DirectWrite può gestire i riferimenti del tipo di carattere per i quali i dati effettivi si trovano in un percorso di rete remoto, nonché quando i dati effettivi sono locali.

Un set di caratteri è un set di riferimenti del tipo di carattere, insieme ad alcune proprietà informative di base che possono essere utilizzate per fare riferimento al tipo di carattere o per confrontarlo con altri tipi di carattere, ad esempio il nome della famiglia o un valore del tipo di carattere. I dati effettivi per i vari tipi di carattere possono essere locali, oppure possono essere tutti remoti o una combinazione.

Un set di caratteri può essere usato per ottenere un oggetto della raccolta dei tipi di carattere corrispondente. Per ulteriori informazioni, vedere set di caratteri e raccolte di tipi di carattere. 

L'interfaccia IDWriteFontSet fornisce metodi che consentono di eseguire query per i valori delle proprietà, ad esempio il nome della famiglia o il tipo di carattere, oppure per i riferimenti del tipo di carattere che corrispondono a valori di proprietà specifici. Dopo aver filtrato fino a una particolare selezione, è possibile ottenere un'istanza dell'interfaccia [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) , con metodi per il download (se i dati effettivi del tipo di carattere sono attualmente remoti), per ottenere l'oggetto [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) corrispondente che può essere utilizzato per il layout e il rendering. 

L'interfaccia IDWriteFontFile è sottostanti ogni tipo di carattere o riferimento al tipo di carattere. Rappresenta il percorso di un file del tipo di carattere e presenta due componenti: un caricatore di file del tipo di carattere e una chiave del file del tipo di carattere. Il caricatore di file del tipo di carattere ([**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)) viene usato per aprire un file, se necessario, e restituisce un flusso con i dati ([**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)). A seconda del caricatore, i dati possono trovarsi in un percorso di file locale, in un URL remoto o in un buffer di memoria. La chiave è un valore definito dal caricatore che identifica in modo univoco il file all'interno del contesto del caricatore, consentendo al caricatore di individuare i dati e creare un flusso per tale file. 

I tipi di carattere personalizzati possono essere facilmente aggiunti a un set di caratteri personalizzato, che a sua volta può essere utilizzato per filtrare o organizzare informazioni sui tipi di carattere per scopi quali la creazione di un'interfaccia utente di selezione del tipo di carattere. Il set di caratteri può essere usato anche per creare una raccolta di tipi di carattere da usare in API di livello superiore, ad esempio [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). L'interfaccia [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) può essere usata per creare un set di caratteri personalizzato che include diversi tipi di carattere personalizzati. Può anche essere usato per creare un set di caratteri personalizzato che combina tipi di carattere personalizzati e tipi di carattere forniti dal sistema; o che combina i tipi di carattere con origini diverse per i dati effettivi, ovvero archiviazione locale, URL remoti e memoria. 

Come indicato in precedenza, un riferimento del tipo di carattere può fare riferimento ai dati del tipo di carattere in un'origine remota, ma i dati devono essere locali per ottenere un oggetto del tipo di carattere che può essere utilizzato per il layout e il rendering. Il download dei dati remoti viene gestito da una coda di download del tipo di carattere. Le app possono usare l'interfaccia [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) per accodare le richieste di download dei tipi di carattere remoti per avviare il processo di download e per registrare un oggetto [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) per eseguire un'azione al termine del processo di download. 

Per la maggior parte delle interfacce descritte di seguito, DirectWrite fornisce le implementazioni di sistema. L'unica eccezione è l'interfaccia [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) , implementata da un'app per eseguire azioni specifiche dell'app quando i tipi di carattere remoti sono stati scaricati localmente. Le app possono avere un motivo per fornire le proprie implementazioni personalizzate per determinate altre interfacce, sebbene siano necessarie solo in scenari specifici e più avanzati. Ad esempio, un'app deve fornire un'implementazione personalizzata dell'interfaccia [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) per gestire i file del tipo di carattere nell'archivio locale che usano il formato del contenitore WOFF2. Di seguito sono riportati altri dettagli. 

## <a name="fonts-and-font-file-formats"></a>Tipi di carattere e formati di file dei tipi di carattere

Un altro concetto chiave utile da comprendere è la relazione tra i singoli tipi di carattere e i file del tipo di carattere che li contengono. L'idea di un file del tipo di carattere OpenType (. ttf o. otf) che contiene un solo tipo di carattere è familiare. Il formato del carattere OpenType, tuttavia, consente anche una raccolta di tipi di carattere OpenType (. TTC o. OTC), che è un singolo file che contiene più tipi di carattere. I file di raccolta OpenType vengono spesso usati per i tipi di carattere di grandi dimensioni strettamente correlati e hanno valori identici per determinati dati del tipo di carattere: combinando i tipi di carattere in un singolo file, i dati comuni possono essere deduplicati. Per questo motivo, un tipo di carattere o un riferimento al tipo di carattere deve riferirsi non solo a un file del tipo di carattere (o a un'origine dati equivalente), ma deve anche specificare un indice del tipo di carattere all'interno di tale file, per il caso generale in cui il file può essere un file di raccolta. 

Per i tipi di carattere utilizzati sul Web, i dati del tipo di carattere vengono spesso compressi in determinati formati di contenitore, WOFF o WOFF2, che forniscono una compressione dei dati del tipo di carattere e un certo livello di protezione contro la pirateria e la violazione delle licenze dei tipi di carattere. Dal punto di vista funzionale, un file WOFF o WOFF2 equivale a un file di tipo carattere o di raccolta di tipi di carattere OpenType, ma i dati vengono codificati in un formato diverso che richiede la decompressione prima di poterlo usare. 

Alcune API DirectWrite possono gestire i singoli tipi di carattere, mentre altre API possono gestire file che potrebbero includere file di raccolta OpenType che contengono più visi. Analogamente, alcune API gestiscono solo i dati in formato OpenType non elaborati, mentre altre API possono gestire i formati di contenitori compressi, WOFF e WOFF2. Questi dettagli sono riportati nella discussione riportata di seguito. 

## <a name="font-sets-and-font-collections"></a>Set di caratteri e raccolte di tipi di carattere

Alcune applicazioni possono essere implementate per lavorare con i tipi di carattere usando l'interfaccia [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) . Esiste una corrispondenza diretta tra una raccolta di tipi di carattere e un set di caratteri. Ognuno può mantenere gli stessi tipi di carattere, ma li presenta con un'altra organizzazione. Da qualsiasi raccolta di tipi di carattere, è possibile ottenere un set di caratteri corrispondente e viceversa.

Quando si lavora con un numero di tipi di carattere personalizzati, è più semplice usare un'interfaccia del generatore di set di caratteri per creare un set di caratteri personalizzato e quindi ottenere una raccolta di tipi di carattere dopo la creazione del set di caratteri. Il processo per la creazione di un set di caratteri personalizzato verrà descritto in dettaglio di seguito. Per ottenere un'interfaccia [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) da un set di caratteri, viene usato il metodo [**IDWriteFactory3:: CreateFontCollectionFromFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-createfontcollectionfromfontset) .

Se l'app dispone di un oggetto raccolta ed è necessario ottenere un set di caratteri corrispondente, è possibile eseguire questa operazione usando il metodo [**IDWriteFontCollection1:: Getfontt**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontcollection1-getfontset) . 

## <a name="common-scenarios"></a>Scenari comuni

In questa sezione vengono descritti alcuni degli scenari più comuni che coinvolgono i set di caratteri personalizzati:

-   Creazione di un set di caratteri personalizzato utilizzando tipi di carattere arbitrari nei percorsi della file system locale.
-   Creazione di un set di caratteri personalizzato con i tipi di carattere noti, ad esempio in bundle con l'app, archiviati nella file system locale.
-   Creazione di un set di caratteri personalizzato utilizzando tipi di carattere remoti noti sul Web.
-   Creazione di un set di caratteri personalizzato utilizzando i dati del tipo di carattere caricati in memoria.

Le implementazioni complete per questi scenari sono disponibili nell' [esempio di set di caratteri personalizzati DirectWrite](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). Questo esempio illustra anche uno scenario più avanzato per la gestione dei dati del tipo di carattere compressi nei formati di contenitore WOFF o WOFF2, che verranno illustrati di seguito. 

### <a name="creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system"></a>Creazione di un set di caratteri utilizzando tipi di carattere arbitrari nell'file system locale

Quando si gestisce un set arbitrario di file di tipi di carattere nella risorsa di archiviazione locale, il metodo [**IDWriteFontSetBuilder1:: AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) è utile in quanto, in una singola chiamata, può gestire tutti i visi dei tipi di carattere all'interno di un file di raccolta dei tipi di carattere OpenType, nonché tutte le istanze per un tipo di carattere della variabile OpenType. Questa opzione è disponibile in Windows 10 Creators Update (versione di anteprima 15021 o successiva) ed è consigliata ogni volta che è disponibile. 

Per usare questo metodo, usare il processo seguente.

<dl> 1. Per iniziare, creare l'interfaccia <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">IDWriteFactory5</a> : 


```C++
IDWriteFactory5* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
  DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



   
2. Usare la factory per ottenere l' <a href=""></a> interfaccia [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) : 


```C++
IDWriteFontSetBuilder1* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
}  
                
```



  
3. Per ogni file del tipo di carattere nel file system locale, creare un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) che vi faccia riferimento: 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



   
4. Aggiungere l'oggetto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) al generatore del set di caratteri usando il metodo [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) : 


```C++
hr = pFontSetBuilder->AddFontFile(pFontFile); 
```

Se il percorso del file specificato nella chiamata a [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) fa riferimento a un elemento diverso da un file OpenType supportato, la chiamata a [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) restituirà un errore, DWrite \_ E \_ FileFormat.

5. Una volta che tutti i file sono stati aggiunti al generatore del set di caratteri, è possibile creare il set di caratteri personalizzato: 


```C++
IDWriteFontSet* pFontSet; 
hr = pFontSetBuilder->CreateFontSet(&pFontSet); 
```



   
</dl>

Se l'app deve essere eseguita in versioni di Windows 10 precedenti a Windows 10 Creators Update, il metodo AddFontFile non sarà disponibile. La disponibilità può essere rilevata creando un'interfaccia [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) e quindi usando QueryInterface per provare a ottenere un'interfaccia [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) : se l'operazione ha esito positivo, saranno disponibili anche l'interfaccia [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) e il metodo [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) .

Se il metodo AddFontFile non è disponibile, è necessario usare il metodo [**IDWriteFontSetBuilder:: AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) per aggiungere singoli visi del tipo di carattere. Per consentire i file della raccolta dei tipi di carattere OpenType che contengono più visi, è possibile usare il metodo [**IDWriteFontFile:: Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) per determinare il numero di visi contenuti all'interno del file. Il processo è il seguente.

<dl> 1. Per iniziare, creare l'interfaccia <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3</a> : 


```C++
IDWriteFactory3* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



  
2. Usare la factory per ottenere l'interfaccia [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) : 


```C++
IDWriteFontSetBuilder* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
} 
```



  
3. Per ogni file del tipo di carattere, creare un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile), come descritto in precedenza: 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



Anziché aggiungere il file direttamente al generatore del set di caratteri, è necessario determinare il numero di visi e creare singoli oggetti [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) .   
4. Usare il metodo [**Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) per ottenere il numero di visi nel file. 


```C++
BOOL isSupported; 
DWRITE_FONT_FILE_TYPE fileType; 
UINT32 numberOfFonts; 
hr = pFontFile->Analyze(&isSupported, &fileType, /* face type */ nullptr, &numberOfFonts); 
```



Il metodo [**Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) imposterà inoltre i valori per i parametri e di FileType supportati. Se il formato del file non è supportato, l'oggetto sarà supportato da FALSE e sarà possibile eseguire un'azione appropriata, ad esempio ignorando il file.   
5. Ciclo sul numero di tipi di carattere impostati nel parametro numberOfFonts. All'interno del ciclo, creare un [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) per ogni coppia di file/indice e aggiungerlo al generatore del set di caratteri. 


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



  
6. Una volta aggiunti tutti i visi al generatore del set di caratteri, creare il set di caratteri personalizzato, come illustrato in precedenza.  
</dl>

Un'app può essere progettata in modo da usare il metodo [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) preferito durante l'esecuzione in Windows 10 Creators Update, ma eseguire il fallback per usare il metodo [**AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) quando si eseguono versioni precedenti di Windows 10. Verificare la disponibilità dell'interfaccia [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) , come descritto in precedenza, quindi creare un branch di conseguenza. Questo approccio è illustrato nell' [esempio di set di caratteri personalizzati DirectWrite](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). 

### <a name="creating-a-font-set-using-known-fonts-in-the-local-file-system"></a>Creazione di un set di caratteri utilizzando i tipi di carattere noti nella file system locale

Come indicato in precedenza, ogni riferimento al tipo di carattere in un set di caratteri è associato a determinate proprietà informative, ad esempio il nome della famiglia e il peso del carattere. Quando si aggiungono tipi di carattere personalizzati a un generatore di set di caratteri usando le chiamate API elencate in precedenza, queste proprietà informative vengono ottenute direttamente dai dati del tipo di carattere effettivi, che viene letto quando viene aggiunto il tipo di carattere. In alcune situazioni, tuttavia, se un'app ha un'altra fonte di informazioni su un tipo di carattere, potrebbe essere necessario fornire i propri valori personalizzati per queste proprietà. 

Come esempio di questo può essere utile, si supponga che un'app bundle alcuni tipi di carattere usati per presentare particolari elementi dell'interfaccia utente all'interno dell'app. In alcuni casi, ad esempio con una nuova versione dell'app, potrebbe essere necessario modificare i tipi di carattere specifici usati dall'app per questi elementi. Se l'app contiene riferimenti codificati a tipi di carattere specifici, la sostituzione di un tipo di carattere con un altro richiede la modifica di ognuno di questi riferimenti. Al contrario, se l'app usa proprietà personalizzate per assegnare alias funzionali in base al tipo di elemento o al testo di cui viene eseguito il rendering, esegue il mapping di ogni alias a un tipo di carattere specifico in un'unica posizione e quindi usa gli alias in tutti i contesti in cui vengono creati e modificati i tipi di carattere, quindi la sostituzione di un tipo di carattere con un altro richiede solo 

I valori personalizzati per le proprietà informative possono essere assegnati quando viene chiamato il metodo [**IDWriteFontSetBuilder:: AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) . Il metodo per eseguire questa operazione è il seguente: Questa operazione può essere usata in qualsiasi versione di Windows 10. 

Come illustrato sopra, iniziare ottenendo le interfacce [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) e [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) . Per aggiungere un tipo di carattere personalizzato, creare un [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference), come illustrato in precedenza. Prima che questo venga aggiunto al generatore del set di caratteri (all'interno del ciclo nel passaggio 5, illustrato sopra), tuttavia, l'app definisce i valori delle proprietà personalizzate da usare. 

Un set di valori di proprietà personalizzati viene definito utilizzando una matrice di strutture di [**\_ \_ proprietà del tipo di carattere DWrite**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) . Ognuna di queste identifica una particolare proprietà dall'enumerazione [**dell' \_ \_ \_ ID della proprietà del tipo di carattere DWrite**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) e il valore della proprietà corrispondente da usare.  

Si noti che tutti i valori delle proprietà sono assegnati come stringhe. Se gli utenti potrebbero essere visualizzati in un secondo momento, è possibile impostare valori alternativi per una determinata proprietà per lingue diverse, ma ciò non è obbligatorio. Si noti anche che, se i valori delle proprietà personalizzate vengono impostati dall'app, solo i valori specificati verranno utilizzati all'interno del set di caratteri. DirectWrite non deriverà alcun valore direttamente dal tipo di carattere per le proprietà informative utilizzate in un set di caratteri. 

Nell'esempio seguente vengono definiti valori personalizzati per tre proprietà informative: il nome della famiglia, il nome completo e lo spessore del carattere. 


```C++
DWRITE_FONT_PROPERTY props[] = 
{ 
  { DWRITE_FONT_PROPERTY_ID_FAMILY_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_FULL_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_WEIGHT, L"400", nullptr } 
}; 
               
            
```



Dopo aver definito la matrice desiderata di valori di proprietà per un tipo di carattere, effettuare una chiamata a AddFontFaceRefence, passando la matrice di proprietà e il riferimento al tipo di carattere. 


```C++
hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference, props, ARRAYSIZE(props)); 
```



 

Una volta che tutti i tipi di carattere personalizzati sono stati aggiunti al generatore del set di caratteri, insieme alle relative proprietà personalizzate, creare il set di caratteri personalizzato, come illustrato in precedenza. 

### <a name="creating-a-custom-font-set-using-known-remote-fonts-on-the-web"></a>Creazione di un set di caratteri personalizzato utilizzando caratteri remoti noti sul Web

Le proprietà personalizzate sono importanti per l'utilizzo di tipi di carattere remoti. Ogni riferimento del tipo di carattere deve contenere alcune proprietà informative per caratterizzare il tipo di carattere e distinguerlo da altri tipi di carattere. Poiché i dati del tipo di carattere per i tipi di carattere remoti non sono locali, DirectWrite non può derivare proprietà direttamente dai dati del tipo di carattere Pertanto, le proprietà devono essere specificate in modo esplicito quando si aggiunge un tipo di carattere remoto al generatore del set di caratteri.

La sequenza di chiamate API per l'aggiunta di tipi di carattere remoti a un set di caratteri è simile alla sequenza descritta per lo scenario precedente. Poiché i dati del tipo di carattere sono remoti, tuttavia, le operazioni necessarie per la lettura dei dati del tipo di carattere effettivi saranno diverse rispetto a quando si utilizzano i file nella risorsa di archiviazione locale. Per questa situazione, è stata aggiunta una nuova interfaccia di livello inferiore, [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader), in Windows 10 Creators Update. 

Per usare il caricatore di file del tipo di carattere remoto, è necessario prima registrarlo con una factory DirectWrite. Il caricatore deve essere mantenuto dall'app per tutto il tempo in cui vengono usati i tipi di carattere associati. Una volta che i tipi di carattere non sono più in uso e, a un certo punto, prima che la Factory venga distrutta, è necessario annullare la registrazione del caricatore. Questa operazione può essere eseguita nel distruttore per la classe proprietaria dell'oggetto Loader. Questa procedura verrà illustrata di seguito. 

Il metodo per la creazione di un set di caratteri personalizzato con i tipi di carattere remoti è il seguente: Questa operazione richiede Windows 10 Creators Update.  

<dl> 1. Creare un'interfaccia IDWriteFactory5, come illustrato in precedenza.   
2. Creare un'interfaccia <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">IDWriteFontSetBuilder</a> , come illustrato in precedenza.   
3. Usare la factory per ottenere un <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader">IDWriteRemoteFontFileLoader</a>. 


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



Viene restituita un'implementazione fornita dal sistema dell'interfaccia del caricatore di file del tipo di carattere remoto che è in grado di gestire le interazioni HTTP per il download dei dati del tipo di carattere per conto dell'app. È possibile specificare un URL del referrer o intestazioni aggiuntive se richiesto dal servizio del tipo di carattere o dai servizi che sono l'origine per i tipi di carattere.    

> [!IMPORTANT]
> Nota sulla sicurezza: quando viene effettuato un tentativo di recupero di un tipo di carattere remoto, esiste il rischio che un utente malintenzionato possa falsificare il server previsto che verrà chiamato. In tal caso, gli URL di destinazione e referrer e i dettagli dell'intestazione vengono divulgati all'autore dell'attacco. Gli sviluppatori di app sono responsabili della mitigazione di questo rischio. È consigliabile usare il protocollo HTTPS, anziché HTTP. 

 

Per più tipi di carattere è possibile usare un singolo caricatore di file del tipo di carattere remoto, anche se è possibile usare diversi caricatori se i tipi di carattere vengono ottenuti da più servizi che hanno requisiti diversi per l'URL del referrer o per intestazioni aggiuntive.   
4. Registrare il caricatore del file del tipo di carattere remoto con la factory. 


```C++
 if (SUCCEEDED(hr)) 
 { 
     hr = pDWriteFactory->RegisterFontFileLoader(pRemoteFontFileLoader); 
 } 
```



Da questo punto, i passaggi per la creazione del set di caratteri personalizzato sono simili a quelli descritti per i file dei tipi di carattere locali noti, con due eccezioni importanti. In primo luogo, l'oggetto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) viene creato usando l'interfaccia del caricatore del file del tipo di carattere remoto anziché usare la factory. In secondo luogo, non è possibile usare il metodo Analyze perché i dati del tipo di carattere non sono locali. Al contrario, l'app deve sapere se il file del tipo di carattere remoto è un file di raccolta dei tipi di carattere OpenType e, in tal caso, deve sapere quali tipi di carattere all'interno della raccolta verrà usato e l'indice per ciascuno di essi. Di conseguenza, i passaggi rimanenti sono i seguenti.   
5. Per ogni file del tipo di carattere remoto, usare l'interfaccia del caricatore del file del tipo di carattere remoto per creare un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile), specificando l'URL necessario per accedere al file del tipo di carattere. 


```C++
 IDWriteFontFile* pFontFile; 
 hr = pRemoteFontFileLoader->CreateFontFileReferenceFromUrl( 
     pDWriteFactory, 
     /* baseUrl */ L"https://github.com/", 
     /* fontFileUrl */ L"winjs/winjs/blob/master/src/fonts/Symbols.ttf?raw=true", 
     &pFontFile 
 ); 
```



Si noti che l'URL completo può essere specificato nel parametro fontFileUrl o può essere suddiviso in parti di base e relative. Se viene specificato un URL di base, la concatenazione dei valori baseUrl e fontFileUrl deve fornire l'URL completo, DirectWrite non fornirà alcun delimitatore aggiuntivo.  

> [!IMPORTANT]
> Nota sulla sicurezza/prestazioni: quando viene effettuato un tentativo di recupero di un tipo di carattere remoto, non c'è alcuna garanzia che Windows riceva una risposta dal server. In alcuni casi, un server può rispondere con un errore di file non trovato per un URL relativo non valido, ma smettere di rispondere se riceve più richieste non valide. Se il server non risponde, si verificherà un timeout di Windows, anche se sono stati avviati più recuperi. È necessario eseguire le operazioni possibili per assicurarsi che gli URL siano validi quando vengono effettuate le chiamate. 

 

Si noti inoltre che l'URL può puntare a un file del tipo di carattere OpenType non elaborato (. ttf,. otf,. TTC,. OTC), ma può anche puntare a tipi di carattere in un file contenitore WOFF o WOFF2. Se si fa riferimento a un file WOFF o WOFF2, l'implementazione DirectWrite del caricatore di file del tipo di carattere remoto decomprimerà automaticamente i dati del tipo di carattere dal file contenitore.   
6. Per ogni indice del tipo di carattere all'interno del file del tipo di carattere remoto da usare, creare un [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference). 


```C++
 IDWriteFontFaceReference* pFontFaceReference; 
 hr = pDWriteFactory->CreateFontFaceReference(pFontFile, /* faceIndex */ 0, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);
```



  
7. Definire le proprietà personalizzate per il tipo di carattere, come illustrato in precedenza.   
8. Aggiungere il riferimento al tipo di carattere insieme alle proprietà personalizzate al generatore del set di caratteri, come illustrato in precedenza.   
9. Dopo che tutti i tipi di carattere sono stati aggiunti al generatore del set di caratteri, creare il set di caratteri, come illustrato in precedenza.   
10. A un certo punto, quando i tipi di carattere remoti non verranno più usati, annullare la registrazione del caricatore del file del tipo di carattere remoto. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pRemoteFontFileLoader); 
```



  
</dl>

Una volta creato un set di caratteri personalizzato con tipi di carattere remoti personalizzati, il set di caratteri contiene riferimenti e proprietà informative per i tipi di carattere remoti, ma i dati effettivi sono ancora remoti. Il supporto DirectWrite per i tipi di carattere remoti consente di mantenere un riferimento al tipo di carattere nel set di caratteri e di selezionare un tipo di carattere da utilizzare per il layout e il rendering, ma i dati effettivi non vengono scaricati fino a quando non è necessario utilizzarlo, ad esempio quando verrà eseguito il layout del testo.  

Un'app può adottare un approccio iniziale richiedendo che DirectWrite scarichi i dati del tipo di carattere e quindi attendendo la conferma di un download riuscito prima che venga avviata un'elaborazione con il tipo di carattere. Tuttavia, un download di rete implica una latenza di durata imprevedibile e anche il successo è incerto. Per questo motivo, in genere è preferibile adottare un approccio diverso, in modo da poter eseguire il layout e il rendering inizialmente usando tipi di carattere alternativi o di fallback già locali, richiedendo il download del tipo di carattere remoto desiderato in parallelo e quindi aggiornando i risultati dopo che il tipo di carattere desiderato è stato scaricato. 

Per richiedere che l'intero tipo di carattere venga scaricato prima che venga usato, è possibile usare il metodo [**IDWriteFontFaceReference:: EnqueueFontDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuefontdownloadrequest) . Se il tipo di carattere è molto grande, solo una parte dei dati potrebbe essere necessaria per l'elaborazione di stringhe specifiche. DirectWrite fornisce metodi aggiuntivi che possono essere usati per richiedere parti dei dati del tipo di carattere necessari per contenuto particolare, [**EnqueueCharacterDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuecharacterdownloadrequest) e [**EnqueueGlyphDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueueglyphdownloadrequest).  

Si supponga che l'approccio da eseguire nell'app consenta di eseguire l'elaborazione inizialmente usando tipi di carattere locali, alternativi o di fallback. Il metodo IDWriteFontFallback::[**MapCharacters**](idwritefontfallback-mapcharacters.md) può essere usato per identificare i tipi di carattere di fallback locali e verrà automaticamente accodato una richiesta di download del tipo di carattere preferito. Se, inoltre, si usa [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e il testo nel layout è formattato con un riferimento a un tipo di carattere remoto, DirectWrite userà automaticamente il metodo **MapCharacters** per ottenere i tipi di carattere di fallback locali e accodare una richiesta di download dei dati del tipo di carattere remoto. 

DirectWrite gestisce una coda di download dei tipi di carattere per ogni factory e le richieste effettuate usando i metodi indicati in precedenza vengono aggiunte a tale coda. La coda di download dei tipi di carattere può essere ottenuta usando il metodo [**IDWriteFactory3:: GetFontDownloadQueue**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getfontdownloadqueue) . 

Se viene eseguita una richiesta di download, ma i dati del tipo di carattere sono già locali, verrà generato un no-op: non verrà aggiunto nulla alla coda di download. Un'app può verificare se la coda è vuota o se sono presenti richieste di download in sospeso chiamando il metodo [**IDWriteFontDownloadQueue:: IsEmpty**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-isempty) . 

Dopo che sono state aggiunte le richieste del tipo di carattere remoto alla coda, è necessario avviare il processo di download. Quando i tipi di carattere remoti vengono usati in [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout), il download viene avviato automaticamente quando l'app chiama i metodi **IDWriteTextLayout** che forzano le operazioni di layout o rendering, ad esempio GetLineMetrics o i metodi di disegno. In altri scenari, l'app deve avviare il download direttamente chiamando [**IDWriteFontDownloadQueue:: BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload).  

Al termine di un download, l'app sarà all'inizio di eseguire le azioni appropriate, ovvero la prosecuzione delle operazioni in sospeso o la ripetizione delle operazioni eseguite inizialmente con i tipi di carattere di fallback. Se viene usato il layout del testo di DirectWrite, [**IDWriteTextLayout3:: InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) può essere usato per cancellare i risultati temporanei calcolati con i tipi di carattere di fallback. Per consentire all'app di ricevere una notifica al termine del processo di download e di eseguire le azioni appropriate, l'app deve fornire un'implementazione dell'interfaccia [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) e passarla alla chiamata BeginDownload. 

> [!IMPORTANT]
> Nota sulla sicurezza/prestazioni: quando viene effettuato un tentativo di recupero di un tipo di carattere remoto, non c'è alcuna garanzia che Windows riceva una risposta dal server. Se il server non risponde, si verificherà un timeout di Windows, anche se l'operazione potrebbe richiedere alcuni minuti se vengono recuperati più tipi di carattere remoti, ma con esito negativo. La chiamata a BeginDownload restituirà immediatamente. Le app non devono bloccare l'interfaccia utente durante l'attesa della chiamata di [**IDWriteFontDownloadListener::D ownloadcompleted**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadlistener-downloadcompleted) . 

 

Le implementazioni di esempio di queste interazioni con la coda di download dei tipi di carattere di DirectWrite e dell'interfaccia [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) sono disponibili nell' [esempio di set di caratteri personalizzati DirectWrite](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)e anche nell'esempio di tipi di carattere [scaricabili DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont). 

### <a name="creating-a-custom-font-set-using-font-data-loaded-into-memory"></a>Creazione di un set di caratteri personalizzato usando i dati del tipo di carattere caricati in memoria

Così come le operazioni di basso livello per la lettura dei dati da un file del tipo di carattere sono diverse per i file in un disco locale rispetto ai file remoti sul Web, lo stesso vale anche per i dati del tipo di carattere caricati in un buffer di memoria. In Windows 10 Creators Update, [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader), è stata aggiunta una nuova interfaccia di basso livello per la gestione dei dati di tipo carattere in memoria. 

Come per un caricatore di file del tipo di carattere remoto, un caricatore di file dei tipi di carattere in memoria deve prima essere registrato con una factory DirectWrite. Il caricatore deve essere mantenuto dall'app per tutto il tempo in cui vengono usati i tipi di carattere associati. Una volta che i tipi di carattere non sono più in uso e, a un certo punto, prima che la Factory venga distrutta, è necessario annullare la registrazione del caricatore. Questa operazione può essere eseguita nel distruttore per la classe proprietaria dell'oggetto Loader. Questa procedura verrà illustrata di seguito. 

Se l'app dispone di informazioni separate sui visi dei tipi di carattere rappresentati dai dati, può aggiungere singoli riferimenti del tipo di carattere a un generatore di set di caratteri con proprietà personalizzate specificate. Poiché i dati del tipo di carattere sono nella memoria locale, tuttavia, questo non è necessario. DirectWrite sarà in grado di leggere direttamente i dati per derivare i valori delle proprietà. 

DirectWrite presuppone che i dati del tipo di carattere siano in formato OpenType non elaborato, equivalente a un file OpenType (. ttf,. otf,. TTC,. OTC), ma in memoria anziché su disco. I dati non possono trovarsi in un formato di contenitore WOFF o WOFF2. I dati possono rappresentare una raccolta di tipi di carattere OpenType. Se non si usano proprietà personalizzate, è possibile usare il metodo [**IDWriteFontSetBuilder1:: AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) per aggiungere tutti i tipi di carattere nei dati in un'unica chiamata. 

Una considerazione importante per lo scenario in memoria è il ciclo di vita dei dati. Se viene fornito un puntatore al buffer a DirectWrite senza una chiara indicazione del proprietario, DirectWrite effettuerà una copia dei dati in un nuovo buffer di memoria di cui sarà proprietario. Per evitare la copia di dati e l'allocazione di memoria aggiuntiva, l'app può passare un oggetto proprietario di dati che implementa IUnknown e che possiede il buffer di memoria contenente i dati del tipo di carattere. Implementando questa interfaccia, DirectWrite può aggiungere al conteggio dei riferimenti dell'oggetto, garantendo in tal modo la durata dei dati di proprietà. 

Il metodo per la creazione di un set di caratteri personalizzato usando i dati di tipo carattere in memoria è il seguente: Questa operazione richiede Windows 10 Creators Update. Si presuppone che un oggetto proprietario di dati implementato dall'app implementi IUnknown e disponga anche di metodi che restituiscono un puntatore al buffer di memoria e la dimensione del buffer. 

<dl> 1. Creare un'interfaccia IDWriteFactory5, come illustrato in precedenza.  
2. Creare un'interfaccia [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) , come illustrato in precedenza.  
3. Usare la factory per ottenere un IDWriteInMemoryFontFileLoader. 


```C++
 IDWriteInMemoryFontFileLoader* pInMemoryFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateInMemoryFontFileLoader(&pInMemoryFontFileLoader); 
}
```



Restituisce un'implementazione fornita dal sistema dell'interfaccia del caricatore di file dei tipi di carattere in memoria.   
4. Registrare il caricatore di file dei tipi di carattere in memoria con la factory. 


```C++
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->RegisterFontFileLoader(pInMemoryFontFileLoader); 
}
```



   
5. Per ogni file di tipo di carattere in memoria, usare il caricatore di file dei tipi di carattere in memoria per creare un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile). 


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



   
6. Aggiungere l'oggetto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) al generatore del set di caratteri usando il metodo [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) , come illustrato in precedenza.  Se è necessario, l'app può invece creare singoli oggetti [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) basati su **IDWriteFontFile**, definire facoltativamente proprietà personalizzate per ogni riferimento al tipo di carattere e quindi aggiungere il riferimento del tipo di carattere con proprietà personalizzate al set di caratteri usando il metodo [**AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) , come illustrato in precedenza.   
7. Dopo che tutti i tipi di carattere sono stati aggiunti al generatore del set di caratteri, creare il set di caratteri personalizzato, come illustrato in precedenza.   
8. A un certo punto, quando i tipi di carattere in memoria non verranno più usati, annullare la registrazione del caricatore di file dei tipi di carattere in memoria. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pInMemoryFontFileLoader);
```



  
</dl>

 

## <a name="advanced-scenarios"></a>Scenari avanzati

Alcune app possono avere requisiti speciali che richiedono un'elaborazione più avanzata rispetto a quanto descritto in precedenza. 

### <a name="combining-font-sets"></a>Combinazione di set di caratteri

Per alcune app potrebbe essere necessario creare un set di caratteri che include una combinazione di elementi di altri set di caratteri. Ad esempio, un'app potrebbe voler creare un set di caratteri che combina tutti i tipi di carattere installati nel sistema con una selezione di tipi di carattere personalizzati o che combina i tipi di carattere installati che corrispondono a determinati criteri con altri tipi di carattere. DirectWrite dispone di API per supportare la manipolazione e la combinazione di set di caratteri. 

Per combinare due o più set di caratteri, il metodo [**IDWriteFontSetBuilder:: AddFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontset) aggiunge tutti i tipi di carattere nel set di caratteri specificato da aggiungere a un generatore di set di caratteri in una singola chiamata. Se nel nuovo set di caratteri sono desiderati solo determinati tipi di carattere di un set di caratteri esistente, è possibile usare il metodo [**IDWriteFontSet:: GetMatchingFonts**](idwritefontset-getmatchingfonts-overload.md) per derivare un nuovo oggetto set di caratteri che è stato filtrato in modo da includere solo i tipi di carattere corrispondenti alle proprietà specificate. Questi metodi forniscono un modo semplice per creare un set di caratteri personalizzato che combina i tipi di carattere di due o più set di caratteri esistenti 

### <a name="using-local-woff-or-woff2-font-data"></a>Uso di dati di tipo carattere WOFF o WOFF2 locali

Se un'app contiene file di tipo carattere nel file system locale o in un buffer di memoria, ma usano i formati di contenitore WOFF o WOFF2, DirectWrite (Windows 10 Creators Update o versioni successive) fornisce un metodo per decomprimere il formato del contenitore, [**IDWriteFactory5:: UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile), che restituisce un [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream). 

Tuttavia, l'app deve essere in grado di ottenere il [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) in un oggetto del caricatore di file del tipo di carattere. Un modo per eseguire questa operazione consiste nel creare un'implementazione [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) personalizzata che esegua il wrapping del flusso. Come per gli altri caricatori di file del tipo di carattere, è necessario registrarlo prima di usarlo e annullarne la registrazione prima che la Factory esca dall'ambito.  

Se il caricatore personalizzato verrà usato anche con i file del tipo di carattere non elaborato (non compresso), l'app dovrà anche fornire un'implementazione personalizzata dell'interfaccia [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) per la gestione di tali file. Sono disponibili più semplici metodi che usano le API descritte in precedenza per la gestione dei file di tipi di carattere non elaborati. La necessità di un'implementazione del flusso personalizzata potrebbe essere evitata usando percorsi di codice distinti per i file di tipo carattere compressi rispetto ai file di tipo carattere non elaborati. 

Dopo la creazione di un oggetto del caricatore di file del tipo di carattere personalizzato, i dati del file del tipo di carattere compresso vengono aggiunti al caricatore da mezzi specifici dell'app. Il caricatore può gestire più file di tipi di carattere, ciascuno dei quali viene identificato usando una chiave definita dall'app che è opaca per DirectWrite. Dopo l'aggiunta di un file del tipo di carattere compresso al caricatore, viene usato il metodo [**IDWriteFactory archiviata nei:: CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) per ottenere un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) in base al caricatore per i dati del tipo di carattere identificati da una chiave specificata.  

È possibile decomprimere effettivamente i dati del tipo di carattere poiché i tipi di carattere vengono aggiunti al caricatore, ma possono anche essere gestiti nel metodo [**IDWriteFontFileLoader:: CreateStreamFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) , che DirectWrite chiamerà quando è necessario leggere prima i dati del tipo di carattere. 

Dopo la creazione di un oggetto IDWriteFontFile, i passaggi rimanenti per aggiungere i tipi di carattere a un set di caratteri personalizzato saranno quelli descritti in precedenza. 

Un'implementazione che usa questo approccio è illustrata nell' [esempio di set di caratteri personalizzati DirectWrite](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). 

### <a name="using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation"></a>Uso di meccanismi di tipo carattere remoto DirectWrite con implementazione di rete di basso livello personalizzata

I meccanismi DirectWrite per la gestione dei tipi di carattere remoti possono essere divisi in meccanismi di livello superiore, con set di tipi di carattere che includono riferimenti ai tipi di carattere per i tipi di carattere remoti, verifica della località dei dati del tipo di carattere e gestione della coda per le richieste di download del tipo di carattere e dei meccanismi di basso livello che gestiscono Alcune app possono voler usare i meccanismi di tipo carattere remoto di livello superiore, ma richiedono anche interazioni di rete personalizzate, ad esempio la comunicazione con i server che usano protocolli diversi da HTTP. 

Per questa situazione, un'app deve creare un'implementazione personalizzata dell'interfaccia [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) che interagisce con altre interfacce di livello inferiore nei modi richiesti. L'app dovrà anche fornire implementazioni personalizzate di queste interfacce di basso livello: [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream)e [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult). Queste tre interfacce hanno metodi di callback che DirectWrite chiamerà durante le operazioni di download. 

Quando viene chiamato [**IDWriteFontDownloadQueue:: BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload) , DirectWrite esegue query sul caricatore di file del tipo di carattere remoto sulla località dei dati e richiede il flusso remoto. Se i dati non sono locali, chiamerà il Metodo BeginDownload del flusso. L'implementazione del flusso non deve bloccarsi sulla chiamata, ma deve restituire immediatamente un oggetto [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) che fornisce l'handle di attesa che DirectWrite utilizzerà per attendere l'operazione di download asincrona. L'implementazione del flusso personalizzato è responsabile della gestione della comunicazione remota. Quando si è verificato l'evento di completamento, DirectWrite chiamerà [**IDWriteAsyncResult:: GetResult**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteasyncresult-getresult) per determinare il risultato dell'operazione. Se il risultato ha esito positivo, si prevede che le successive chiamate ReadFragment al flusso per gli intervalli scaricati vengano eseguite correttamente. 

> [!IMPORTANT]
> Nota sulla sicurezza/prestazioni: quando viene effettuato un tentativo di recupero di un tipo di carattere remoto, il potenziale esiste in generale perché un utente malintenzionato possa falsificare il server previsto chiamato o che il server non risponde. Se si implementano interazioni di rete personalizzate, è possibile che si disponga di un maggiore controllo sulle mitigazioni rispetto a quando si gestiscono server di terze parti. Tuttavia, spetta all'utente prendere in considerazione le mitigazioni appropriate per evitare la divulgazione di informazioni o un attacco Denial of Service. Sono consigliati protocolli sicuri, ad esempio HTTPS. Inoltre, è necessario compilare un timeout in modo che l'handle di evento restituito a DirectWrite venga impostato. 

 

### <a name="supporting-scenarios-on-earlier-windows-versions"></a>Scenari di supporto nelle versioni precedenti di Windows

Gli scenari descritti possono essere supportati in DirectWrite nelle versioni precedenti di Windows, ma richiedono un'implementazione molto più personalizzata della parte dell'app usando le API più limitate disponibili prima di Windows 10. Per ulteriori informazioni, vedere [raccolte di tipi di carattere personalizzati (Windows 7/8)](custom-font-collections.md).

 

 