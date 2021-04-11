---
description: Modello concettuale
ms.assetid: f906466e-acdc-4d0f-bf27-c5a25dc56c01
title: Modello concettuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a17538e7fdb454fa8eb61ab951a3316b0f0c327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233009"
---
# <a name="the-conceptual-model"></a>Modello concettuale

In questa sezione vengono descritti gli oggetti, le proprietà e le risorse che costituiscono il modello concettuale WPD.

### <a name="objects"></a>Oggetti

In WPD, le entità logiche nei dispositivi sono definite oggetti. In genere, ma non sempre, rappresentano i dati nel dispositivo. Gli oggetti dispongono di proprietà a cui fanno riferimento gli identificatori di oggetto. Esempi di oggetti includono immagini e cartelle in una fotocamera, canzoni e playlist su un lettore multimediale, contatti su un telefono cellulare e così via.

Gli oggetti possono anche rappresentare parti funzionali o informative del dispositivo. Esempi di questi includono i controlli dei giocatori (riproduzione/record/pausa), le impostazioni della fotocamera, le funzionalità SMS di un telefono cellulare e così via.

I due argomenti seguenti forniscono esempi e illustrazioni di due tipi di oggetti: l'oggetto Image e l'oggetto Mediacast.

### <a name="image-object"></a>Image (oggetto)

Un oggetto Image rappresenta un'immagine ancora. Il diagramma seguente mostra le relazioni tra un oggetto immagine, le relative proprietà e le relative risorse.

![diagramma che mostra un oggetto WPD e la relativa relazione con le relative proprietà e risorse](images/wpd-overview-figure2.gif)

Per ulteriori informazioni sull'oggetto Image e sulle relative proprietà, vedere l'argomento relativo all' [**\_ immagine del \_ tipo \_ di contenuto WPD**](wpd-content-type-image.md) .

### <a name="mediacast-object"></a>Oggetto Mediacast

Un oggetto Mediacast può essere considerato come un oggetto contenitore che raggruppa il contenuto correlato, così come una playlist di gruppi di musica. Spesso, un oggetto Mediacast viene usato per raggruppare il contenuto multimediale pubblicato online. Un canale RSS, ad esempio, può essere rappresentato come un oggetto Mediacast i cui riferimenti a oggetti puntano a oggetti contenuto che rappresentano ogni elemento nel canale. Il diagramma seguente illustra la relazione tra un oggetto Mediacast e i tre oggetti audio in esso contenuti.

![diagramma che mostra la struttura gerarchica di un oggetto medica e di tre oggetti in esso contenuti](images/mediacast1.gif)

I riferimenti all'oggetto audio sono specificati nella proprietà [riferimenti a \_ oggetti \_ WPD](object-properties.md) per l'oggetto Mediacast. Per ulteriori informazioni sulle proprietà supportate da un oggetto Mediacast, vedere l'argomento relativo al [**\_ \_ \_ \_ cast del tipo di contenuto WPD**](wpd-content-type-media-cast.md) .

### <a name="properties"></a>Proprietà

Le proprietà dell'oggetto forniscono un meccanismo per lo scambio di metadati che descrivono oggetti. Ad esempio, un oggetto Image può includere proprietà che descrivono il nome file, le dimensioni, il formato, la larghezza in pixel e così via.

Le proprietà hanno un valore corrente, nonché gli attributi. WPD definisce un set di proprietà standard che costituiscono le definizioni di API e DDI. I fornitori non sono limitati alle proprietà WPD predefinite e possono aggiungerne di propri.

### <a name="property-attributes"></a>Attributi di proprietà

Gli attributi delle proprietà descrivono i diritti di accesso, i valori validi e altre informazioni correlate a una proprietà. Ad esempio, la proprietà che rappresenta la velocità in bit può essere un intervallo compreso tra 8 kilobit al secondo (Kbps) e 20 kbps con un valore di passaggio di 1 Kbps.

I diritti di accesso indicano se i chiamanti possono leggere, scrivere e/o eliminare la proprietà. I valori validi indicano restrizioni per i valori delle proprietà. I valori validi sono detti di un formato specifico. I formati di valore validi includono intervallo, ovvero la proprietà può assumere un valore da min a max con il passaggio specificato, enumerazione (ovvero, il valore della proprietà è uno di quelli nell'elenco specificato) e None (ovvero non sono presenti valori validi specifici).

### <a name="resources"></a>Risorse

Le risorse sono segnaposto per dati binari. Un oggetto può avere più di una risorsa. Se, ad esempio, l'oggetto rappresenta un file di immagine con un'annotazione audio, le risorse per questo oggetto potrebbero essere le seguenti:

-   Risorsa predefinita. Questa risorsa rappresenta l'intero file di immagine. Sono inclusi dati incorporati, ad esempio annotazioni audio, anteprime e così via.
-   Una risorsa di anteprima. Questa risorsa rappresenta i dati di anteprima per l'immagine.
-   Una risorsa di annotazione audio. Questa risorsa rappresenta i dati audio associati all'immagine.

### <a name="resource-attributes"></a>Attributi delle risorse

Analogamente agli attributi delle proprietà, gli attributi delle risorse descrivono i diritti di accesso, le dimensioni, il formato e altre informazioni correlate a una risorsa. Ad esempio, gli attributi per una risorsa di annotazione audio in un oggetto Image possono specificare la velocità in bit, il numero di canali e il formato dati dell'audio.

### <a name="rendering-profiles-and-resource-attributes"></a>Profili di rendering e attributi delle risorse

Il profilo di rendering è un metodo usato dalle applicazioni per individuare gli attributi validi per una determinata risorsa. Ad esempio, un telefono cellulare può supportare bitmap con restrizioni specifiche sui valori di larghezza e altezza minimi e massimi. Eseguendo una query sui profili di rendering per l'oggetto bitmap, un'applicazione può recuperare i valori esatti.

Nell'output di esempio seguente vengono identificate le informazioni sul profilo di rendering restituite dal dispositivo se sono supportate bitmap con un'altezza minima di 10 pixel, una larghezza minima di 20 pixel, un'altezza massima di 1000 pixel e una larghezza massima di 2000 pixel.


```C++
WPD_OBJECT_FORMAT = WPD_OBJECT_FORMAT_BMP
WPD_MEDIA_HEIGHT:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  10
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  10 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_MEDIA_WIDTH:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX =  2000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE = 0
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  2000 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
```



Vedere l'argomento [recupero delle funzionalità di rendering supportate da un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md) nella Guida alla programmazione per una descrizione del modo in cui l'applicazione può recuperare un profilo di rendering e gli attributi delle risorse associati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica dell'applicazione**](application-overview.md)
</dt> </dl>

 

 



