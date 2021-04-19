---
title: Interfacce DirectWrite
description: Elenca le interfacce definite da DirectWrite.
ms.assetid: 7075e771-ce34-4426-8c07-13e85ff4d453
keywords:
- DirectWrite, interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0297875bfe4b5f0a0610091f7330a427ed51b822
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320346"
---
# <a name="directwrite-interfaces"></a>Interfacce DirectWrite

DirectWrite definisce le interfacce seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) | Rappresenta il risultato di un'operazione asincrona. Un client può utilizzare l'interfaccia per attendere il completamento dell'operazione e ottenere il risultato.  |
| [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) | Incapsula una bitmap indipendente dal dispositivo a 32 bit e un contesto di dispositivo, che può essere usato per il rendering dei glifi. |
| [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1) | Incapsula una bitmap indipendente dal dispositivo a 32 bit e un contesto di dispositivo, che è possibile usare per il rendering dei glifi. |
| [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) | Incapsula una bitmap indipendente dal dispositivo a 32 bit e un contesto di dispositivo, che può essere usato per il rendering dei glifi. |
| [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) | Questa interfaccia consente all'applicazione di enumerare le esecuzioni del glifo dei colori. |
| [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) | Enumeratore per una raccolta ordinata di esecuzioni del glifo dei colori. |
| [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) | Utilizzato per creare tutti gli oggetti DirectWrite successivi. Questa interfaccia è l'interfaccia Factory radice per tutti gli oggetti DirectWrite. |
| [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) | Interfaccia Factory radice per tutti gli oggetti [DirectWrite](direct-write-portal.md) . |
| [**IDWriteFactory2**](idwritefactory2.md) | Interfaccia Factory radice per tutti gli oggetti [DirectWrite](direct-write-portal.md) . |
| [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) | Interfaccia Factory radice per tutti gli oggetti [DirectWrite](direct-write-portal.md) . |
| [**IDWriteFactory4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory4) | Interfaccia Factory radice per tutti gli oggetti DirectWrite. |
| [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) | Interfaccia Factory radice per tutti gli oggetti DirectWrite. |
| [**IDWriteFactory6**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) | Rappresenta un oggetto Factory da cui vengono creati tutti gli oggetti DirectWrite. **IDWriteFactory6** aggiunge nuove funzionalità per l'utilizzo di tipi di carattere e risorse dei tipi di carattere. |
| [**IDWriteFactory7**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) | Questa interfaccia rappresenta un oggetto Factory da cui vengono creati tutti gli oggetti DirectWrite. **IDWriteFactory7** aggiunge nuove funzionalità per l'utilizzo di tipi di carattere di sistema. |
| [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | Rappresenta un tipo di carattere fisico in una raccolta di tipi di carattere. Questa interfaccia viene usata per creare i visi dei tipi di carattere da tipi di carattere fisici o per recuperare informazioni come le metriche del tipo di carattere o i nomi dei visi da quelli esistenti. |
| [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) | Rappresenta un tipo di carattere fisico in una raccolta di tipi di carattere. |
| [**IDWriteFont2**](idwritefont2.md) | Rappresenta un tipo di carattere fisico in una raccolta di tipi di carattere. |
| [**IDWriteFont3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3) | Rappresenta un tipo di carattere in una raccolta di tipi di carattere. |
| [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) | Oggetto che incapsula un set di tipi di carattere, ad esempio il set di tipi di carattere installati nel sistema, o il set di tipi di carattere in una directory specifica. L'API della raccolta dei tipi di carattere può essere usata per individuare le famiglie di caratteri e i tipi di carattere disponibili e per ottenere alcuni metadati sui tipi di carattere. |
| [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) | Oggetto che incapsula un set di tipi di carattere, ad esempio il set di tipi di carattere installati nel sistema, o il set di tipi di carattere in una directory specifica. L'API della raccolta dei tipi di carattere può essere usata per individuare le famiglie di caratteri e i tipi di carattere disponibili e per ottenere alcuni metadati sui tipi di carattere. |
| [**IDWriteFontCollection2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) | Questa interfaccia incapsula un set di tipi di carattere, ad esempio il set di tipi di carattere installati nel sistema o il set di tipi di carattere in una directory specifica. |
| [**IDWriteFontCollection3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) | Questa interfaccia incapsula un set di tipi di carattere, ad esempio il set di tipi di carattere installati nel sistema o il set di tipi di carattere in una directory specifica. |
| [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) | Usato per costruire una raccolta di tipi di carattere in base a un particolare tipo di chiave.  |
| [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) | Interfaccia di callback definita dall'applicazione che riceve le notifiche dalla coda di download dei tipi di carattere (interfaccia [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) ). I callback vengono eseguiti nel thread di download e gli oggetti devono essere preparati a gestire le chiamate sui rispettivi metodi da altri thread in qualsiasi momento. |
| [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) | Interfaccia che accoda le richieste di download per i caratteri remoti, i caratteri, i glifi e i frammenti del tipo di carattere.  |
| [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) | Questa interfaccia espone vari dati di tipo carattere, ad esempio le metriche, i nomi e le strutture di glifi. Contiene il tipo di carattere, i riferimenti ai file appropriati e i dati di identificazione della faccia. |
| [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) | Contiene il tipo di carattere, i riferimenti ai file appropriati e i dati di identificazione della faccia.  |
| [**IDWriteFontFace2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontface2) | Questa interfaccia contiene il tipo di carattere, i riferimenti ai file appropriati e i dati di identificazione della faccia. Viene aggiunta la possibilità di controllare se un percorso di rendering del colore è potenzialmente necessario.  |
| [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) | Contiene il tipo di carattere, i riferimenti ai file appropriati e i dati di identificazione della faccia. |
| [**IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4) | Contiene il tipo di carattere, i riferimenti ai file appropriati e i dati di identificazione della faccia. |
| [**IDWriteFontFace5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) | Questa interfaccia contiene il tipo di carattere, i riferimenti ai file appropriati e i dati di identificazione della faccia. Aggiunge nuove funzionalità, ad esempio il confronto di due facce del tipo di carattere, il recupero dei valori dell'asse del tipo di carattere e il recupero della risorsa di tipo carattere sottostante. |
| [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) | Rappresenta un riferimento a un tipo di carattere. Un riferimento che identifica in modo univoco un tipo di carattere, da cui è possibile creare un tipo di carattere per eseguire query sulle metriche dei tipi di carattere e utilizzarlo per il rendering. Un riferimento al tipo di carattere è costituito da un file del tipo di carattere, dall'indice del tipo di carattere e dalla simulazione della faccia È possibile che i dati del file non siano ancora fisicamente presenti nel computer locale.  |
| [**IDWriteFontFaceReference1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) | Rappresenta un riferimento a un tipo di carattere. Un riferimento che identifica in modo univoco un tipo di carattere, da cui è possibile creare un tipo di carattere per eseguire query sulle metriche dei tipi di carattere e utilizzarlo per il rendering. |
| [**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback) | Consente di accedere ai tipi di carattere di fallback dall'elenco dei tipi di carattere. |
| [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) | Consente di creare mapping di fallback dei tipi di carattere Unicode e di creare un oggetto del tipo di carattere che esegue il fallback da tali mapping. |
| [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) | Rappresenta una famiglia di tipi di carattere correlati. |
| [**IDWriteFontFamily1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily1) | Rappresenta una famiglia di tipi di carattere correlati. |
| [**IDWriteFontFamily2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) | Rappresenta una famiglia di tipi di carattere correlati. **IDWriteFontFamily2** aggiunge nuove funzionalità, incluso il recupero dei tipi di carattere per i valori dell'asse del tipo di carattere. |
| [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) | Rappresenta un file del tipo di carattere. Le applicazioni, ad esempio i gestori dei tipi di carattere o i visualizzatori di tipi di carattere, possono chiamare [**IDWriteFontFile:: Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) per verificare se un determinato file è un file di tipo carattere e se è un tipo di carattere supportato dal sistema di tipi di carattere. |
| [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) | Incapsula una raccolta di file di tipi di carattere. Il sistema dei tipi di carattere utilizza questa interfaccia per enumerare i file del tipo di carattere durante la compilazione di una raccolta |
| [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) | Gestisce il caricamento delle risorse del file del tipo di carattere di un determinato tipo da una chiave di riferimento del file del tipo di carattere in un oggetto flusso di file  |
| [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) | Carica i dati del file del tipo di carattere da un caricatore di file del tipo di carattere  |
| [**IDWriteFontList**](/windows/win32/api/dwrite/nn-dwrite-idwritefontlist) | Rappresenta un elenco di tipi di carattere. |
| [**IDWriteFontList1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist1) | Rappresenta un elenco di tipi di carattere. |
| [**IDWriteFontList2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) | Rappresenta un elenco di tipi di carattere. **IDWriteFontList2** aggiunge nuove funzionalità, incluso il recupero del set di caratteri sottostante usato dall'elenco. |
| [**IDWriteFontResource**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) | nn-dwrite_3-idwritefontresource |
| [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) | Rappresenta un set di caratteri. |
| [**IDWriteFontSet1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) | Rappresenta un set di caratteri. |
| [**IDWriteFontSet2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) | Rappresenta un set di caratteri. |
| [**IDWriteFontSet3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) | Rappresenta un set di caratteri. |
| [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) | Contiene i metodi per la compilazione di un set di caratteri. |
| [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) | Contiene i metodi per la compilazione di un set di caratteri. |
| [**IDWriteFontSetBuilder2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) | Contiene i metodi per la compilazione di un set di caratteri. |
| [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) | Fornisce l'interoperabilità con GDI, ad esempio i metodi per convertire un tipo di carattere in una struttura LOGFONT o per convertire una descrizione del tipo di carattere GDI in un tipo di carattere. Viene inoltre utilizzato per creare oggetti di destinazione di rendering bitmap. |
| [**IDWriteGdiInterop1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1) | Fornisce l'interoperabilità con GDI, ad esempio i metodi per convertire un tipo di carattere in una struttura LOGFONT o per convertire una descrizione del tipo di carattere GDI in un tipo di carattere. Viene inoltre utilizzato per creare oggetti di destinazione di rendering bitmap. |
| [**IDWriteGeometrySink**](idwritegeometrysink.md) | [**IDWriteGeometrySink**](idwritegeometrysink.md) è un **typedef** dell'interfaccia [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) . Per ulteriori informazioni, vedere la pagina di riferimento di [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) . |
| [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) | Contiene informazioni di basso livello utilizzate per eseguire il rendering di un'esecuzione del glifo. |
| [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) | Esegue il wrapping di un elemento grafico inline definito dall'applicazione, consentendo a DWrite di eseguire query sulle metriche come se il grafico fosse un glifo inline con il testo. |
| [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) | Rappresenta un caricatore di file del tipo di carattere che può accedere a tipi di carattere in memoria. |
| [**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md) | Implementazione incorporata dell'interfaccia [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) , che opera sui file del tipo di carattere locale ed espone le informazioni sul file di tipo di carattere locale dalla chiave di riferimento del file del tipo di carattere. I riferimenti ai file del tipo di carattere creati con [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) usano questo caricatore di file di tipo |
| [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) | Rappresenta una raccolta di stringhe indicizzate in base al nome delle impostazioni locali. |
| [**IDWriteNumberSubstitution**](./idwritenumbersubstitution.md) | Include le cifre appropriate e la punteggiatura numerica per le impostazioni locali specificate. |
| [**IDWritePixelSnapping**](/windows/win32/api/dwrite/nn-dwrite-idwritepixelsnapping) | Definisce le proprietà di blocco dei pixel, ad esempio i pixel per DIP (pixel indipendente dal dispositivo) e la matrice di trasformazione corrente di un renderer di testo. |
| [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) | Rappresenta un caricatore di file del tipo di carattere che può accedere a tipi di carattere remoti, ovvero scaricabili.  |
| [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) | Rappresenta un flusso di file del tipo di carattere, parti di che possono essere non locali.  |
| [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) | Rappresenta le impostazioni di rendering del testo, ad esempio il livello ClearType, il contrasto migliorato e la correzione gamma per la rasterizzazione e il filtraggio dei glifi. Un'applicazione ottiene in genere un oggetto parametri di rendering chiamando il metodo [**IDWriteFactory archiviata nei:: CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) . |
| [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1) | Rappresenta le impostazioni di rendering del testo per la rasterizzazione e il filtro dei glifi. |
| [**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2) | Rappresenta le impostazioni di rendering del testo per la rasterizzazione e il filtro dei glifi. |
| [**IDWriteRenderingParams3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriterenderingparams3) | Rappresenta le impostazioni di rendering del testo per la rasterizzazione e il filtro dei glifi. |
| [**IDWriteStringList**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritestringlist) | Rappresenta una raccolta di stringhe indicizzate per numero. |
| [**IDWriteTextAnalysisSink**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink) | Questa interfaccia viene implementata dal client dell'analizzatore di testo per ricevere l'output di un'analisi del testo specificata.  |
| [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) | Interfaccia implementata per ricevere l'output degli analizzatori di testo. |
| [**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) | Implementato dal client dell'analizzatore di testo per fornire testo all'analizzatore. Consente la separazione tra la visualizzazione logica del testo come flusso continuo di caratteri identificabili da posizioni univoche del testo e il layout di memoria effettivo di blocchi di testo potenzialmente discreti nell'archivio di backup del client.  |
| [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) | Interfaccia implementata per fornire le informazioni necessarie all'analizzatore di testo, ad esempio il testo e le proprietà di testo associate. |
| [**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer) | Analizza varie proprietà di testo per l'elaborazione di script complessi, ad esempio il supporto bidirezionale (BiDi) per lingue quali l'arabo, la determinazione delle opportunità di interruzione di riga, la posizione del glifo e la sostituzione dei numeri. |
| [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) | Analizza varie proprietà di testo per l'elaborazione di script complessi. |
| [**IDWriteTextAnalyzer2**](idwritetextanalyzer2.md) | Analizza varie proprietà di testo per l'elaborazione di script complessi. |
| [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) | L'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) descrive le proprietà del tipo di carattere e di paragrafo usate per formattare il testo e descrive le informazioni sulle impostazioni locali.  |
| [**IDWriteTextFormat1**](idwritetextformat1.md) | Descrive le proprietà dei tipi di carattere e paragrafi usati per formattare il testo e descrive le informazioni sulle impostazioni locali.  |
| [**IDWriteTextFormat2**](idwritetextformat2.md) | Descrive le proprietà dei tipi di carattere e paragrafi usati per formattare il testo e descrive le informazioni sulle impostazioni locali.  |
| [**IDWriteTextFormat3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) | Descrive le proprietà dei tipi di carattere e paragrafi usati per formattare il testo e descrive le informazioni sulle impostazioni locali. |
| [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) | L'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) rappresenta un blocco di testo dopo che è stato completamente analizzato e formattato. |
| [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) | Rappresenta un blocco di testo dopo che è stato completamente analizzato e formattato. |
| [**IDWriteTextLayout2**](idwritetextlayout2.md) | Rappresenta un blocco di testo dopo che è stato completamente analizzato e formattato. |
| [**IDWriteTextLayout3**](idwritetextlayout3.md) | Rappresenta un blocco di testo dopo che è stato completamente analizzato e formattato.  |
| [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) | Rappresenta un set di callback definiti dall'applicazione che eseguono il rendering di testo, oggetti inline e decorazioni, ad esempio sottolineature. |
| [**IDWriteTextRenderer1**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextrenderer1) | Rappresenta un set di callback definiti dall'applicazione che eseguono il rendering di testo, oggetti inline e decorazioni, ad esempio sottolineature.  |
| [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) | Rappresenta un'impostazione tipografia del tipo di carattere. |