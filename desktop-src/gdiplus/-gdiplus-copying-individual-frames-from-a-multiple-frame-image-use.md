---
title: Copiare singoli fotogrammi da un'immagine a più fotogrammi
description: Nell'esempio seguente vengono recuperati i singoli fotogrammi da un file TIFF con più frame.
ms.assetid: dfed0b61-2230-4911-a642-0a6e4beb08d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398df806ad56b65114b0cc9a986ea53061183fa4658872b65b7d08ef7e38a9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115101"
---
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a>Copiare singoli fotogrammi da un'immagine a più fotogrammi

Nell'esempio seguente vengono recuperati i singoli fotogrammi da un file TIFF con più frame. Quando è stato creato il file TIFF, i singoli fotogrammi sono stati aggiunti alla dimensione Pagina (vedere Creazione e salvataggio di [un'Multiple-Frame Image](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)). Il codice visualizza ognuna delle quattro pagine e salva ogni pagina in un file disco PNG separato.

Il codice costruisce un [**oggetto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file TIFF a più frame. Per recuperare i singoli fotogrammi (pagine), il codice chiama il [**metodo Image::SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) dell'oggetto **Image.** Il primo argomento passato al metodo **Image::SelectActiveFrame** è l'indirizzo di un GUID che specifica la dimensione in cui i frame sono stati aggiunti in precedenza al file TIFF a più frame. Il GUID FrameDimensionPage è definito in Gdiplusimaging.h. Altri GUID definiti nel file di intestazione sono FrameDimensionTime e FrameDimensionResolution. Il secondo argomento passato al **metodo Image::SelectActiveFrame** è l'indice in base zero della pagina desiderata.

Il codice si basa sulla funzione helper GetEncoderClsid, illustrata in Recupero dell'identificatore di classe [per un codificatore.](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)


```
GUID   pageGuid = FrameDimensionPage;
CLSID  encoderClsid;
Image  multi(L"Multiframe.tif");

// Get the CLSID of the PNG encoder.
GetEncoderClsid(L"image/png", &encoderClsid);

// Display and save the first page (index 0).
multi.SelectActiveFrame(&pageGuid, 0);
graphics.DrawImage(&multi, 10, 10);
multi.Save(L"Page0.png", &encoderClsid, NULL);

// Display and save the second page.
multi.SelectActiveFrame(&pageGuid, 1);
graphics.DrawImage(&multi, 200, 10);
multi.Save(L"Page1.png", &encoderClsid, NULL);

// Display and save the third page.
multi.SelectActiveFrame(&pageGuid, 2);
graphics.DrawImage(&multi, 10, 150);
multi.Save(L"Page2.png", &encoderClsid, NULL);

// Display and save the fourth page.
multi.SelectActiveFrame(&pageGuid, 3);
graphics.DrawImage(&multi, 200, 150);
multi.Save(L"Page3.png", &encoderClsid, NULL);
```



La figura seguente mostra le singole pagine visualizzate dal codice precedente.

![figura che mostra una forma geometrica, una foto a colori, una foto monocromatica e una forma geometrica diversa](images/multiframe1.png)

 

 



