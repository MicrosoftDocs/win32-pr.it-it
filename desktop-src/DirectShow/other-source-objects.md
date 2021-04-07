---
description: Altri oggetti di origine
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: Altri oggetti di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c76c8f6cb104e87630f178a82d613675b96723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747050"
---
# <a name="other-source-objects"></a>Altri oggetti di origine

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Oltre alle origini video e audio, i [servizi di modifica DirectShow](directshow-editing-services.md) (des) supportano gli oggetti di origine seguenti.

**Immagini ancora**

DES supporta i formati di file seguenti per le immagini ancora:

-   Bitmap (.bmp)
-   GIF (Graphics Interchange Format)
-   JPEG (Joint Photographic Experts Group)
-   Targa o scheda grafica TrueVision (. tga): modalità 2 (RGB non compresso) in formato a 16 bit, 24, bit o 32 bit.

Questi file possono essere usati come immagini ancora o per creare animazioni. Per i file bitmap, JPEG e targa, se si usa il file come immagine ancora, chiamare il metodo [**IAMTimelineSrc:: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) per impostare la frequenza dei fotogrammi su zero.

**Sequenze DIB**

Data una serie di file bitmap, JPEG o targa, il motore di rendering può costruire una sequenza DIB. Per creare una sequenza DIB, assegnare i nomi numerici sequenziali ai file, ad esempio Image001.bmp, Image002.bmp, Image003.bmp e così via. Usare il primo file nella sequenza come origine. Impostare la frequenza dei fotogrammi per la sequenza chiamando [**IAMTimelineSrc:: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md). Il motore di rendering scorre le immagini nella sequenza in base alla frequenza dei fotogrammi specificata.

Se la sequenza è troppo corta per riempire la durata, data la frequenza dei fotogrammi, il resto della durata è nero a tinta unita. Non si verificano errori durante il rendering.

**Origini GIF**

DES supporta le origini GIF, incluse le gif animate e trasparenti, usando la specifica GIF89a. Con un GIF animato, a differenza degli altri tipi di file, non è necessario impostare la frequenza dei fotogrammi. Il file GIF specifica il ritardo tra le singole immagini nell'animazione.

Per supportare le gif trasparenti, DES converte le aree trasparenti nell'immagine nel RGB RGB RGB (0, 0, 0). È quindi possibile usare la [transizione della chiave](key-transition.md) per la chiave su RGB (0, 0, 0).

DES converte anche le aree nere che rientrano nell'intervallo RGB (0-7, 0-7, 0-7) nel valore RGB (8, 8, 8), ad eccezione dell'indice di trasparenza, se rientra in tale intervallo. Questa conversione non è rilevabile a occhio.

**Origine colore video**

L'oggetto di [origine colore video](video-color-source.md) crea un'immagine video continua di un colore a tinta unita. Un utilizzo di questo oggetto consiste nel renderlo un livello in una transizione. Ad esempio, usarla in una dissolvenza video o in una dissolvenza in uscita.

**Filtri di origine personalizzati**

I DES possono usare un filtro di origine DirectShow come origine della sequenza temporale, se il filtro soddisfa le condizioni seguenti:

-   Supporta la ricerca
-   Produce un formato supportato da DES. Il formato può essere compresso purché il sistema dell'utente disponga di un filtro DirectShow in grado di decodificarlo.

Per utilizzare un'origine personalizzata, specificare il CLSID del filtro come GUID dell'oggetto di origine. Per ulteriori informazioni, vedere [sottooggetti](subobjects.md). Per supportare le proprietà personalizzate, implementarle come proprietà "put" di **IDispatch** . Negli oggetti di origine sono supportate solo le proprietà statiche. le proprietà dinamiche non sono supportate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di origini](working-with-sources.md)
</dt> </dl>

 

 



