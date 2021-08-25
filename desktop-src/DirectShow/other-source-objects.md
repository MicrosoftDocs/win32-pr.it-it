---
description: Altri oggetti di origine
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: Altri oggetti di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8bbc1618cb7a76e87a4837fce3905a7c9ba7455b13297e779b8be8e80c40732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790911"
---
# <a name="other-source-objects"></a>Altri oggetti di origine

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Oltre alle origini video e audio, [DirectShow Editing Services](directshow-editing-services.md) (DES) supporta gli oggetti di origine seguenti.

**Immagini fisse**

DES supporta i formati di file seguenti per le immagini fisse:

-   Bitmap (.bmp)
-   GIF (Graphics Interchange Format)
-   JPEG (Joint Photographic Experts Group)
-   Adattatore grafica Diao Truevision (.tga): modalità 2 (RGB non compresso) in formato a 16 bit, 24,bit o 32 bit.

Questi file possono essere usati come immagini fisse o per creare animazioni. Per i file bitmap, JPEG e Targa, se si usa il file come immagine fissa, chiamare il metodo [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) per impostare la frequenza dei fotogrammi su zero.

**Sequenze DIB**

Dato una serie di file bitmap, JPEG o Targa, il motore di rendering può costruire una sequenza DIB. Per creare una sequenza DIB, assegnare ai file nomi numericamente sequenziali, ad esempio Image001.bmp, Image002.bmp, Image003.bmp e così via. Usare il primo file della sequenza come origine. Impostare la frequenza dei fotogrammi per la sequenza chiamando [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md). Il motore di rendering scorre le immagini nella sequenza alla frequenza dei fotogrammi specificata.

Se la sequenza è troppo breve per riempire la durata, data la frequenza dei fotogrammi, il resto della durata è nero a tinta unita. Non si verifica alcun errore durante il rendering.

**Origini GIF**

DES supporta le origini GIF, tra cui GIF animate e trasparenti, usando la specifica GIF89a. Con una GIF animata, a differenza degli altri tipi di file, non è necessario impostare la frequenza dei fotogrammi. Il file GIF specifica il ritardo tra ogni immagine nell'animazione.

Per supportare le GIF trasparenti, DES converte le aree trasparenti nell'immagine in RGB tripletta RGB(0,0,0). È quindi possibile usare la [transizione chiave](key-transition.md) a su RGB(0,0,0).

DES converte anche le aree nere che rientrano nell'intervallo RGB(0–7,0–7,0-7) nel valore RGB(8,8,8), ad eccezione dell'indice di trasparenza, se rientra in tale intervallo. Questa conversione non è rilevabile per l'occhio.

**Origine colore video**

[L'oggetto Origine colore](video-color-source.md) video crea un'immagine video continua di colore a tinta unita. Un uso per questo oggetto è renderlo un livello in una transizione. Ad esempio, usarlo in un video con dissolvenza in entrata o in uscita.

**Filtri di origine personalizzati**

DES può usare un DirectShow di origine come origine sequenza temporale, se il filtro soddisfa le condizioni seguenti:

-   Supporta la ricerca
-   Produce un formato supportato da DES. Il formato può essere compresso purché il sistema dell'utente abbia un filtro DirectShow in grado di decodificarlo.

Per usare un'origine personalizzata, specificare il CLSID del filtro come GUID del sottooggetto dell'oggetto di origine. Per altre informazioni, vedere [Subobjects](subobjects.md). Per supportare le proprietà personalizzate, implementarle come proprietà "put" **di IDispatch.** Solo le proprietà statiche sono supportate sugli oggetti di origine. Le proprietà dinamiche non sono supportate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle origini](working-with-sources.md)
</dt> </dl>

 

 



