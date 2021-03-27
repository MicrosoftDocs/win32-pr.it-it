---
title: Copiare singoli frame da un'immagine a più fotogrammi
description: Nell'esempio seguente vengono recuperati i singoli frame da un file TIFF a più frame.
ms.assetid: dfed0b61-2230-4911-a642-0a6e4beb08d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6bdb5668bcebb9babcbcb7d07839694750aec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227086"
---
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a>Copiare singoli frame da un'immagine a più fotogrammi

Nell'esempio seguente vengono recuperati i singoli frame da un file TIFF a più frame. Quando il file TIFF è stato creato, i singoli frame sono stati aggiunti alla dimensione della pagina (vedere [creazione e salvataggio di un'immagine di Multiple-Frame](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)). Il codice visualizza ognuna delle quattro pagine e salva ogni pagina in un file di disco PNG separato.

Il codice costruisce un oggetto [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file TIFF a più frame. Per recuperare i singoli frame (pagine), il codice chiama il metodo [**Image:: SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) di tale oggetto **Image** . Il primo argomento passato al metodo **Image:: SelectActiveFrame** è l'indirizzo di un GUID che specifica la dimensione in cui i frame sono stati aggiunti in precedenza al file TIFF a più frame. Il GUID FrameDimensionPage è definito in Gdiplusimaging. h. Altri GUID definiti in tale file di intestazione sono FrameDimensionTime e FrameDimensionResolution. Il secondo argomento passato al metodo **Image:: SelectActiveFrame** è l'indice in base zero della pagina desiderata.

Il codice si basa sulla funzione helper GetEncoderClsid, che viene illustrata nel [recupero dell'identificatore di classe per un codificatore](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


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



Nella figura seguente sono illustrate le singole pagine visualizzate dal codice precedente.

![illustrazione che mostra una forma geometrica, una foto a colori, una foto monocromatica e una forma geometrica diversa](images/multiframe1.png)

 

 



