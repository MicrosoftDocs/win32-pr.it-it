---
description: Questo argomento introduce il nuovo schema XMP (Extensible Metadata Platform) e la proprietà Photo System. Photo. PeopleNames di Windows 7 che consente l'assegnazione di tag a singoli utenti in una foto digitale.
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: Cenni preliminari sull'assegnazione di tag agli utenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f2080e51d4d340474e0610fcce9512fc72429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131894"
---
# <a name="people-tagging-overview"></a>Cenni preliminari sull'assegnazione di tag agli utenti

Questo argomento introduce il nuovo schema XMP (Extensible Metadata Platform) e la proprietà Photo [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) di Windows 7 che consente l'assegnazione di tag a singoli utenti in una foto digitale. In questo argomento viene inoltre illustrato come utilizzare l'API di Windows Imaging Component (WIC) per leggere e scrivere i metadati necessari per l'assegnazione di tag agli utenti.

In questo argomento sono contenute le sezioni seguenti.

-   [Prerequisiti](#prerequisites)
-   [Introduzione](#introduction)
-   [Assegnazione di tag agli utenti](#people-tagging-overview)
    -   [Nomi di persone](#people-names)
    -   [Rettangoli people](#people-rectangles)
-   [Riferimento allo schema](#schema-reference)
    -   [Schema di Microsoft Photo 1,2](#microsoft-photo-12-schema)
    -   [Schema Microsoft Photo RegionInfo](#microsoft-photo-regioninfo-schema)
    -   [Schema area foto Microsoft](#microsoft-photo-regioninfo-schema)
    -   [Metadati di esempio](#sample-metadata)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Per comprendere questo argomento, è necessario avere familiarità con le interfacce del decodificatore WIC e i componenti di Component Object Model correlati (COM), come descritto in [Panoramica dei componenti di Windows Imaging](-wic-about-windows-imaging-codec.md). Consente inoltre di avere una conoscenza generale dei metadati di imaging, in particolare XMP.

## <a name="introduction"></a>Introduzione

Microsoft ha creato un nuovo schema XMP per l'assegnazione di tag alle persone all'interno di un'immagine digitale. Questo schema consente alle applicazioni di archiviare i nomi e i percorsi di singoli utenti presenti nell'immagine come metadati all'interno dell'immagine. Oltre al nuovo schema, la nuova proprietà Photo [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) è disponibile in Windows 7. Questa nuova proprietà consente alle applicazioni di leggere i nomi dei singoli archiviati nei metadati dell'immagine. WIC utilizza queste nuove funzionalità consentendo alle applicazioni di leggere e scrivere facilmente i metadati per l'assegnazione di tag a foto digitali.

## <a name="people-tagging"></a>Assegnazione di tag agli utenti

WIC fornisce agli sviluppatori di applicazioni i componenti COM che leggono i dati delle immagini e i metadati delle immagini. Per la lettura e la scrittura di metadati, ad esempio la nuova funzionalità di assegnazione di tag agli utenti, WIC fornisce le interfacce [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) e [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) . Queste interfacce consentono alle applicazioni di usare il [linguaggio di query dei metadati](-wic-codec-metadataquerylanguage.md) per scrivere i metadati nei singoli frame di un'immagine. Nella sezione seguente viene illustrato come leggere e scrivere i metadati per l'assegnazione di tag alle persone nei metadati di un'immagine usando Reader e writer di query WIC.

### <a name="people-names"></a>Nomi di persone

Parte della funzionalità di assegnazione di tag agli utenti è la possibilità di ottenere semplicemente un elenco dei nomi delle persone contrassegnate all'interno dell'immagine. Questa parte della funzionalità è supportata dai gestori di metadati [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) e WIC. L'interfaccia [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) , in combinazione con la proprietà System. Photo. PeopleNames, viene usata per leggere i nomi delle persone identificate in un'immagine e archiviate nei metadati dell'immagine.

Nell'esempio di codice seguente viene illustrato un lettore di query ottenuto da un frame immagine per eseguire una query sui metadati di un'immagine per i nomi con tag della proprietà [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) .


```C++
// Not shown: image decoding, retrieving an image frame. 
...
PROPVARIANT value;
IWICMetadataQueryReader *pQueryReader = NULL;
...
// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

// Query for the System.Photo.PeopleNames property.
if (SUCCEEDED(hr))
{
    // Get the property metadata by property name.
    hr = pQueryReader->GetMetadataByName(L"System.Photo.PeopleNames", &value);
}
```



L'espressione di query "System. Photo. PeopleNames" esegue una query sul frame per la proprietà. Se i metadati per l'assegnazione di tag sono presenti e contengono i nomi delle persone, il valore [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) verrà impostato su VT \_ LPWSTR e il valore dei dati conterrà l'elenco dei nomi con tag. Per altre informazioni sulla lettura dei metadati delle immagini, vedere [Cenni preliminari sulla lettura e scrittura dei metadati delle immagini](-wic-codec-readingwritingmetadata.md).

L'esecuzione di query per il tag People names è utile solo se l'immagine contiene effettivamente i metadati di Tag people. Per eseguire questa operazione, un'applicazione deve prima di tutto scriverla. Per scrivere i metadati dei nomi di persone, usare un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) e il percorso XMP esplicito dei metadati. Nell'esempio di codice riportato di seguito viene illustrato l'utilizzo di un writer di query per scrivere un nome nel percorso della query.


```C++
// Not shown: image encoding, retrieving/creating the image frame,
// creating the IWICImagingFactory 
...
IWICImagingFactory *pFactory = NULL;
IWICMetadataQueryWriter *pQueryWriter = NULL;
...
// Get the query writer from the image frame.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pQueryWriter);
}

// A query writer specifically for this person's XMP struct
IWICMetadataQueryWriter *pXMPStructQueryWriter = NULL;

// Create a query writer specifically for an XMP Struct
hr = pFactory->CreateQueryWriter(
    GUID_MetadataFormatXMPStruct,
    NULL,
    &pXMPStructQueryWriter
    );

// Create a variant representing the structure created above
PROPVARIANT xmpStruct;
PropVariantInit(&xmpStruct);

// VT_UNKNOWN indicates that we're setting a COM object, in this case a XMPStruct
// which will hold the name and rectangle
xmpStruct.vt = VT_UNKNOWN; 
xmpStruct.punkVal = pXMPStructQueryWriter;

if(SUCCEEDED(hr))
{
    // WIC will automatically create the xmp base, the RegionInfo struct, and the Regions
    // bag (an unordered array) but structs within that bag need to be explicitly created.
    // The {ulong=0} in the query means to insert the new struct at the start of the bag,
    // {} could also be used to insert at the end of the bag.
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions/{ulong=0}",
        &xmpStruct
        );
}

// Set up the PROPVARIANT with the name information
PROPVARIANT personName;
PropVariantInit(&personName);
personName.vt = VT_LPWSTR;
personName.pwszVal = L"John Doe";

if(SUCCEEDED(hr))
{
    // Set the name metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:PersonDisplayName",
        &personName
        );  
}
```



Si noti il passaggio che costruisce la struttura XMP e la relativa impostazione `MPRI:Regions/{ulong=0}` . Senza questo passaggio, WIC non è in grado di identificare la posizione in cui posizionare il `PersonDisplayName` in un secondo momento. Si noti inoltre che viene utilizzato il percorso di query esplicito anziché [System. Photo. PeopleNames](-wic-photoprop-system-photo-peoplenames.md), i cui criteri dei metadati non supportano la scrittura di metadati.

### <a name="people-rectangles"></a>Rettangoli people

I nomi delle persone, tuttavia, fanno parte della funzionalità di assegnazione di tag degli utenti. Oltre a archiviare i nomi delle persone nei metadati, lo schema supporta anche le informazioni sull'area che identificano l'area specifica (un rettangolo) che la persona viene visualizzata nell'immagine.

Le informazioni sul rettangolo sono rappresentate da quattro valori decimali delimitati da virgole, ad esempio "0,25, 0,25, 0,25, 0,25". I primi due valori specificano la coordinata superiore sinistra; gli ultimi due specificano l'altezza e la larghezza del rettangolo. Le dimensioni dell'immagine ai fini della definizione dei rettangoli people vengono normalizzate su 1, il che significa che nell'esempio "0,25, 0,25, 0,25, 0,25", il rettangolo inizia con 1/4 della distanza dalla parte superiore e 1/4 della distanza dalla sinistra dell'immagine. Sia l'altezza che la larghezza del rettangolo sono pari a 1/4 della dimensione delle rispettive dimensioni di immagine.

Le informazioni sul rettangolo che identificano i singoli vengono scritte nello stesso modo in cui vengono scritti i nomi delle persone, all'interno della stessa struttura. Per scrivere i metadati del rettangolo, usare un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) e il percorso XMP esplicito dei metadati. Nell'esempio di codice seguente viene continuato l'esempio precedente e viene aggiunto un rettangolo che rappresenta ' John Doe ' ai metadati dell'immagine. Si noti che usa lo stesso `{ulong=0}` indice per associare il rettangolo a "John Doe".


```C++
// Set up the PROPVARIANT with the rectangle information
PROPVARIANT rectangle;
PropVariantInit(&rectangle);
rectangle.vt = VT_LPWSTR;
rectangle.pwszVal = L"0.0,0.0,0.25,0.25";

if(SUCCEEDED(hr))
{
    // Set the rectangle metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:Rectangle",
        &rectangle
        );
}
```



## <a name="schema-reference"></a>Riferimenti agli schemi

Gli schemi Microsoft XMP per la codifica di persone definiscono un set di proprietà per contrassegnare i singoli utenti nelle foto digitali.

Le sezioni seguenti forniscono le definizioni dello schema necessarie per l'assegnazione di tag agli utenti. Laddove possibile, le definizioni dello schema utilizzano le convenzioni fornite dalle [specifiche di Adobe Extensible Metadata Platform (XMP)](https://www.adobe.com/devnet/xmp/). Le definizioni dello schema in questo argomento illustrano lo spazio dei nomi XML Uniform Resource Identifier (URI) che identifica lo schema e il prefisso dello spazio dei nomi dello schema preferito, seguito da una tabella in cui sono elencate tutte le proprietà definite per lo schema. Ogni tabella contiene le colonne seguenti:

-   **Proprietà** : nome della proprietà, incluso il prefisso dello spazio dei nomi preferito.

-   **Tipo valore** : tipo di valore della proprietà. Gli schemi di supporto per l'assegnazione di tag degli utenti usano i tipi di valore XMP, quando possibile, inclusi data e testo. I tipi di matrice sono preceduti dal tipo di contenitore: `alt` , `bag` o `seq` .

-   **Category** : le proprietà dello schema sono interne o esterne:

    -   I metadati interni devono essere impostati dall'applicazione.

    -   I metadati esterni devono essere impostati dall'utente e sono indipendenti dal contenuto del documento.

-   **Descrizione** : Descrizione della proprietà.

### <a name="microsoft-photo-12-schema"></a>Schema di Microsoft Photo 1,2

Lo schema Microsoft Photo 1,2 fornisce un set di proprietà per le aree dell'immagine.

-   L'URI dello spazio dei nomi dello schema è `https://ns.microsoft.com/photo/1.2/` .
-   Il prefisso dello spazio dei nomi dello schema preferito è `MP` .



| Proprietà      | Tipo di valore | Category | Descrizione                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| MP: RegionInfo | RegionInfo | Interno | **obbligatorio** : archivia la radice dei metadati per l'assegnazione di tag agli utenti. Vedere la sezione schema di Microsoft Photo RegionInfo che segue. |



 

### <a name="microsoft-photo-regioninfo-schema"></a>Schema Microsoft Photo RegionInfo

Lo schema Microsoft Photo RegionInfo 1,2 fornisce un set di proprietà per informazioni sull'area.

-   L'URI dello spazio dei nomi dello schema è `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .
-   Il prefisso dello spazio dei nomi dello schema preferito è `MPRI` .



| Proprietà              | Tipo di valore | Category | Descrizione                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| MPRI:DateRegionsValid | Data       | Esterno | **facoltativo** : data di creazione dell'ultima area.                                                          |
| MPRI: aree          | Area del contenitore | Esterno | **obbligatorio** : archivia le aree di tag degli utenti. Vedere la sezione relativa allo schema dell'area di foto Microsoft riportata di seguito. |



 

### <a name="microsoft-photo-region-schema"></a>Schema area foto Microsoft

Lo schema Microsoft Photo Region 1,2 fornisce un set di proprietà per le aree dell'immagine.

-   L'URI dello spazio dei nomi dello schema è `https://ns.microsoft.com/photo/1.2/t/Region#` .
-   Il prefisso dello spazio dei nomi dello schema preferito è `MPReg` .



| MPReg: Proprietà          | Tipo di valore | Category | Descrizione                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MPReg:PersonDisplayName | Testo       | Esterno | **obbligatorio** : archivia il nome della persona nel rettangolo specificato.                                                                                                                                                                                                                                            |
| MPReg: rettangolo         | Testo       | Esterno | **facoltativo** : archivia il rettangolo che identifica la persona all'interno della foto. Il rettangolo viene archiviato come quattro valori decimali delimitati da virgole. I primi due valori specificano la coordinata superiore sinistra; gli ultimi due specificano l'altezza e la larghezza del rettangolo. I valori decimali devono essere normalizzati in 1. |
| MPReg:PersonEmailDigest | Testo       | Esterno | **facoltativo** : archivia l'hash del messaggio crittografato SHA-1 dell'indirizzo di posta elettronica attivo della persona.                                                                                                                                                                                                                     |
| MPReg:PersonLiveIdCID   | Testo       | Esterno | **facoltativo** : archivia la rappresentazione decimale con segno del CID attivo della persona, un intero a 64 bit che identifica pubblicamente un'identità Live.                                                                                                                                                                     |



 

### <a name="sample-metadata"></a>Metadati di esempio

Di seguito è riportata una rappresentazione dei metadati XMP per l'assegnazione di tag alle persone.

``` syntax
<rdf:Description rdf:about="" xmlns:MP="https://ns.microsoft.com/photo/1.2/">
<MP:RegionInfo> 
<rdf:Description xmlns:MPRI="https://ns.microsoft.com/photo/1.2/t/RegionInfo#">
   <MPRI:Regions> 
       <rdf:Bag> 
          <rdf:li> 
       <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#"> 
           <MPReg:Rectangle>0.790650, 0.441734, 0.209350, 0.279133
           </MPReg:Rectangle>
           <MPReg:PersonDisplayName>John Doe</MPReg:PersonDisplayName> 
           <MPReg:PersonEmailDigest>2FD4E1C67A2D28FCED849EE1BB76E7391B93EB13</MPReg:PersonEmailDigest> 
           <MPReg:PersonLiveIdCID>1234567890123456789</MPReg:PersonLiveIdCID> 
       </rdf:Description> 
         </rdf:li> 
         <rdf:li>
             <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#">
                  <MPReg:Rectangle>0.222656, 0.302083, 0.378906, 0.505208</MPReg:Rectangle> 
                  <MPReg:PersonDisplayName>Jane Doe</MPReg:PersonDisplayName> 
              </rdf:Description> 
         </rdf:li> 
<!-- Addition Regions --> ... 
<rdf:li>...
</rdf:li> 
</rdf:Bag> 
</MPRI:Regions> </rdf:Description> </MP:RegionInfo> </rdf:Description>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Cenni preliminari sui metadati WIC](-wic-about-metadata.md)
</dt> <dt>

[Panoramica della lettura e della scrittura dei metadati delle immagini](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Cenni preliminari sul linguaggio di query dei metadati](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
