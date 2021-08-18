---
description: Diversi formati di file di immagine consentono di archiviare i metadati insieme a un'immagine.
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: Costanti dei tag delle proprietà Image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509caf20659628909d225bb2dc34a4dbaa27047c08e361b28e9777141f213751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117696419"
---
# <a name="image-property-tag-constants"></a>Costanti dei tag delle proprietà Image

Diversi formati di file di immagine consentono di archiviare i metadati insieme a un'immagine. I metadati sono informazioni su un'immagine, ad esempio titolo, larghezza, modello di fotocamera e artista. Windows GDI+ offre un modo uniforme per archiviare e recuperare metadati dai file di immagine nei formati Tagged Image File Format (TIFF), JPEG, Portable Network Graphics (PNG) e ExIF (Exchangeable Image File).

In GDI+, una parte di metadati è denominata elemento di proprietà *e* un singolo elemento di proprietà viene identificato da una costante numerica denominata tag *di proprietà*. È possibile archiviare e recuperare metadati chiamando i metodi [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) e [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) della classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e non è necessario preoccuparsi dei dettagli del modo in cui un particolare formato di file archivia i metadati.

Negli argomenti seguenti vengono elencati e descritti gli elementi delle proprietà supportati da GDI+. Le descrizioni sono brevi e generali in modo che si applicino a un'ampia gamma di formati di file. Per una descrizione dettagliata dell'uso di un elemento di proprietà in un formato di file specifico, vedere la specifica per tale formato di file. Per collegamenti a diverse specifiche del formato di file, vedere [Specifiche del formato file di immagine](-gdiplus-constant-image-file-format-specifications.md). Per altre informazioni sui metadati, vedere [Reading and Writing Metadata](-gdiplus-reading-and-writing-metadata-use.md) and Image Property Tag Type [**Constants**](-gdiplus-constant-image-property-tag-type-constants.md).

-   [Tag di proprietà in ordine numerico](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [Tag di proprietà in ordine alfabetico](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [Descrizioni degli elementi delle proprietà](-gdiplus-constant-property-item-descriptions.md)

 

 



