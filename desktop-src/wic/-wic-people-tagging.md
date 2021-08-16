---
description: Questo argomento presenta il nuovo schema XMP (Extensible Metadata Platform) e la proprietà Windows 7 photo System.Photo.PeopleNames che consente l'assegnazione di tag a singoli utenti in una foto digitale.
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: Panoramica dell'assegnazione di tag alle persone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a262acd70474f75689e99a3bcd1087cd0117ae3602b78a90357aa932fdd7fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205706"
---
# <a name="people-tagging-overview"></a>Panoramica dell'assegnazione di tag alle persone

Questo argomento presenta il nuovo schema XMP (Extensible Metadata Platform) e la proprietà Windows 7 photo [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) che consente l'assegnazione di tag a singoli utenti in una foto digitale. Questo argomento illustra anche come usare l'API wic (Windows Imaging Component) per leggere e scrivere i metadati necessari per l'assegnazione di tag agli utenti.

In questo argomento sono contenute le sezioni seguenti.

-   [Prerequisiti](#prerequisites)
-   [Introduzione](#introduction)
-   [Assegnazione di tag alle persone](#people-tagging-overview)
    -   [Nomi delle persone](#people-names)
    -   [Rettangoli di persone](#people-rectangles)
-   [Informazioni di riferimento sullo schema](#schema-reference)
    -   [Microsoft Photo 1.2 Schema](#microsoft-photo-12-schema)
    -   [Microsoft Photo RegionInfo Schema](#microsoft-photo-regioninfo-schema)
    -   [Schema dell'area di Microsoft Photo](#microsoft-photo-regioninfo-schema)
    -   [Metadati di esempio](#sample-metadata)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Per comprendere questo argomento, è necessario avere familiarità con le interfacce del decodificatore WIC e i componenti COM (Component Object Model) correlati, come descritto nella panoramica del componente di Windows [Imaging](-wic-about-windows-imaging-codec.md). Consente inoltre di avere una familiarità generale con i metadati di creazione dell'immagine, in particolare XMP.

## <a name="introduction"></a>Introduzione

Microsoft ha creato un nuovo schema XMP per l'assegnazione di tag alle persone all'interno di un'immagine digitale. Questo schema consente alle applicazioni di archiviare i nomi e i percorsi degli utenti che si trova nell'immagine come metadati all'interno dell'immagine. Oltre al nuovo schema, la nuova proprietà photo [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) è disponibile in Windows 7. Questa nuova proprietà consente alle applicazioni di leggere i nomi dei singoli archiviati nei metadati dell'immagine. WIC usa queste nuove funzionalità consentendo alle applicazioni di leggere e scrivere facilmente i metadati delle persone che contrassegnano i metadati nelle foto digitali.

## <a name="people-tagging"></a>Assegnazione di tag alle persone

WIC fornisce agli sviluppatori di applicazioni componenti COM che leggono i dati delle immagini e i metadati dell'immagine. Per la lettura e la scrittura di metadati, ad esempio la nuova funzionalità di assegnazione di tag people, WIC fornisce le [**interfacce IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) e [**IWICMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) Queste interfacce consentono alle applicazioni di usare il [linguaggio di query dei](-wic-codec-metadataquerylanguage.md) metadati per scrivere metadati nei singoli fotogrammi di un'immagine. La sezione seguente illustra come leggere e scrivere i metadati di assegnazione di tag agli utenti nei metadati di un'immagine usando lettori e writer di query WIC.

### <a name="people-names"></a>Nomi delle persone

Parte della funzionalità di assegnazione di tag alle persone è la possibilità di ottenere semplicemente un elenco dei nomi delle persone contrassegnate all'interno dell'immagine. Questa parte della funzionalità è supportata dai gestori di metadati [system.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) e WIC. [**L'interfaccia IWICMetadataQueryReader,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) insieme alla proprietà System.Photo.PeopleNames, viene usata per leggere i nomi delle persone identificate in un'immagine e archiviate nei metadati dell'immagine.

Nell'esempio di codice seguente viene illustrato un lettore di query ottenuto da una cornice di immagine per eseguire query sui metadati di un'immagine per i nomi con tag della proprietà [System.Photo.PeopleNames.](../properties/props-system-photo-peoplenames.md)


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



L'espressione di query "System.Photo.PeopleNames" esegue una query sul frame per la proprietà . Se i metadati di assegnazione di tag people esistono e contengono i nomi delle persone, il valore [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) verrà impostato su VT LPWSTR e il valore dei dati conterrà l'elenco di nomi con \_ tag. Per altre informazioni sulla lettura dei metadati dell'immagine, vedere [Panoramica della lettura e della scrittura dei metadati dell'immagine.](-wic-codec-readingwritingmetadata.md)

L'esecuzione di query per il tag people names è utile solo se l'immagine contiene effettivamente i metadati di assegnazione di tag people. A tale scopo, un'applicazione deve prima di tutto scriverla. Per scrivere i metadati dei nomi delle persone, usare [**un oggetto IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) e il percorso XMP esplicito dei metadati. Nell'esempio di codice seguente viene illustrato l'uso di un writer di query per scrivere un nome nel percorso della query.


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



Si noti il passaggio che crea la struttura XMP e la imposta in `MPRI:Regions/{ulong=0}` . Senza questo passaggio, il WiC non è in grado di identificare la posizione in cui posizionare l'oggetto `PersonDisplayName` in un secondo momento. Si noti anche che viene usato il percorso di query esplicito anziché [System.Photo.PeopleNames](-wic-photoprop-system-photo-peoplenames.md), i cui criteri di metadati non supportano la scrittura di metadati.

### <a name="people-rectangles"></a>Rettangoli di persone

I nomi delle persone, tuttavia, fanno solo parte della funzionalità di assegnazione di tag alle persone. Oltre a archiviare i nomi delle persone nei metadati, lo schema supporta anche informazioni sull'area che identificano l'area specifica (un rettangolo) visualizzata nell'immagine.

Le informazioni sul rettangolo sono rappresentate da quattro valori decimali delimitati da virgole, ad esempio "0,25, 0,25, 0,25, 0,25". I primi due valori specificano la coordinata superiore sinistra. gli ultimi due specificano l'altezza e la larghezza del rettangolo. Le dimensioni dell'immagine ai fini della definizione dei rettangoli delle persone vengono normalizzate su 1, il che significa che nell'esempio "0.25, 0.25, 0.25, 0.25" il rettangolo inizia 1/4 della distanza dalla parte superiore e 1/4 della distanza dalla sinistra dell'immagine. Sia l'altezza che la larghezza del rettangolo sono 1/4 delle dimensioni delle rispettive dimensioni dell'immagine.

Le informazioni sul rettangolo che identificano le persone vengono scritte nello stesso modo in cui vengono scritti i nomi delle persone, all'interno della stessa struttura. Per scrivere i metadati del rettangolo, usare [**un oggetto IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) e il percorso XMP esplicito dei metadati. L'esempio di codice seguente continua l'esempio precedente e aggiunge un rettangolo che rappresenta "John Doe" ai metadati dell'immagine. Si noti che usa lo stesso `{ulong=0}` indice per associare questo rettangolo a 'John Doe'.


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

Gli schemi Microsoft XMP per l'assegnazione di tag agli utenti definiscono un set di proprietà per contrassegnare singoli utenti nelle foto digitali.

Le sezioni seguenti forniscono le definizioni dello schema necessarie per l'assegnazione di tag agli utenti. Laddove possibile, le definizioni dello schema usano le convenzioni fornite dalle specifiche [XMP (Extensible Metadata Platform) di Adobe.](https://www.adobe.com/devnet/xmp/) Le definizioni dello schema in questo argomento illustrano l'URI (XML Namespace Uniform Resource Identifier) che identifica lo schema e il prefisso dello spazio dei nomi dello schema preferito, seguito da una tabella che elenca tutte le proprietà definite per lo schema. Ogni tabella include le colonne seguenti:

-   **Proprietà:** nome della proprietà, incluso il prefisso dello spazio dei nomi preferito.

-   **Tipo di** valore: tipo di valore della proprietà. Gli schemi di supporto per l'assegnazione di tag alle persone usano i tipi di valore XMP quando possibile, inclusi Date e Text. I tipi di matrice sono preceduti dal tipo di contenitore: `alt` `bag` , o `seq` .

-   **Categoria:** le proprietà dello schema sono interne o esterne:

    -   I metadati interni devono essere impostati dall'applicazione.

    -   I metadati esterni devono essere impostati dall'utente ed è indipendente dal contenuto del documento.

-   **Descrizione:** descrizione della proprietà.

### <a name="microsoft-photo-12-schema"></a>Microsoft Photo 1.2 Schema

Lo schema di Microsoft Photo 1.2 fornisce un set di proprietà per le aree immagine.

-   L'URI dello spazio dei nomi dello schema è `https://ns.microsoft.com/photo/1.2/` .
-   Il prefisso dello spazio dei nomi dello schema preferito è `MP` .



| Proprietà      | Tipo di valore | Category | Descrizione                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| MP:RegionInfo | Regioninfo | Interno | **required** : archivia la radice dei metadati di assegnazione di tag alle persone. Vedere la sezione Microsoft Photo RegionInfo Schema che segue. |



 

### <a name="microsoft-photo-regioninfo-schema"></a>Microsoft Photo RegionInfo Schema

Lo schema Microsoft Photo RegionInfo 1.2 fornisce un set di proprietà per le informazioni sull'area.

-   L'URI dello spazio dei nomi dello schema è `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .
-   Il prefisso dello spazio dei nomi dello schema preferito è `MPRI` .



| Proprietà              | Tipo di valore | Category | Descrizione                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| MPRI:DateRegionsValid | Data       | Esterno | **facoltativo:** data di creazione dell'ultima area.                                                          |
| MPRI:Regions          | Area del contenitore | Esterno | **required** : archivia le aree di assegnazione tag degli utenti. Vedere la sezione Schema dell'area foto Microsoft che segue. |



 

### <a name="microsoft-photo-region-schema"></a>Schema dell'area foto Microsoft

Lo schema Microsoft Photo Region 1.2 fornisce un set di proprietà per le aree immagine.

-   L'URI dello spazio dei nomi dello schema è `https://ns.microsoft.com/photo/1.2/t/Region#` .
-   Il prefisso dello spazio dei nomi dello schema preferito è `MPReg` .



| MPReg:Property          | Tipo di valore | Category | Descrizione                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MPReg:PersonDisplayName | Testo       | Esterno | **required:** archivia il nome della persona nel rettangolo specificato.                                                                                                                                                                                                                                            |
| MPReg:Rectangle         | Testo       | Esterno | **facoltativo:** archivia il rettangolo che identifica la persona all'interno della foto. Il rettangolo viene archiviato come quattro valori decimali delimitati da virgole. I primi due valori specificano la coordinata superiore sinistra; Gli ultimi due specificano l'altezza e la larghezza del rettangolo. I valori decimali devono essere normalizzati a 1. |
| MPReg:PersonEmailDigest | Testo       | Esterno | **facoltativo:** archivia l'hash del messaggio crittografato SHA-1 dell'indirizzo di posta elettronica live della persona.                                                                                                                                                                                                                     |
| MPReg:PersonLiveIdCID   | Testo       | Esterno | **facoltativo:** archivia la rappresentazione decimale firmata del CID live della persona, un intero a 64 bit che identifica pubblicamente un'identità live.                                                                                                                                                                     |



 

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

[Windows Cenni preliminari sul componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Panoramica dei metadati WIC](-wic-about-metadata.md)
</dt> <dt>

[Panoramica della lettura e della scrittura dei metadati delle immagini](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Panoramica del linguaggio di query sui metadati](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
