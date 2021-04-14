---
description: Diversi formati di file di immagine consentono di archiviare i metadati insieme a un'immagine.
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: Costanti Tag proprietà immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea9a6c3b8ea7ad9f0693032d3bc779bc414d9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979087"
---
# <a name="image-property-tag-constants"></a>Costanti Tag proprietà immagine

Diversi formati di file di immagine consentono di archiviare i metadati insieme a un'immagine. I metadati sono informazioni su un'immagine, ad esempio titolo, larghezza, modello di fotocamera e artista. Windows GDI+ fornisce un modo uniforme per archiviare e recuperare i metadati dai file di immagine nei formati Tagged Image File Format (TIFF), JPEG, Portable Network Graphics (PNG) e file di immagine scambiabile (EXIF).

In GDI+, una parte di metadati viene chiamata *elemento della proprietà* e un singolo elemento di proprietà viene identificato da una costante numerica denominata *tag di proprietà*. È possibile archiviare e recuperare i metadati chiamando i metodi [**Image:: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) e [**Image:: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) della classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e non è necessario preoccuparsi dei dettagli relativi all'archiviazione dei metadati in un formato di file specifico.

Negli argomenti seguenti vengono elencati e descritti gli elementi della proprietà supportati da GDI+. Le descrizioni sono brevi e generali in modo da essere valide per diversi formati di file. Per una descrizione dettagliata della modalità di utilizzo di un elemento di proprietà in un formato di file specifico, vedere la specifica del formato di file. Per i collegamenti a diverse specifiche del formato di file, vedere [specifiche del formato del file di immagine](-gdiplus-constant-image-file-format-specifications.md). Per ulteriori informazioni sui metadati, vedere la pagina relativa alla [lettura e scrittura](-gdiplus-reading-and-writing-metadata-use.md) di [**costanti di tipo di tag di proprietà Image**](-gdiplus-constant-image-property-tag-type-constants.md)e di metadati.

-   [Tag di proprietà in ordine numerico](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [Tag di proprietà in ordine alfabetico](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [Descrizioni degli elementi delle proprietà](-gdiplus-constant-property-item-descriptions.md)

 

 



