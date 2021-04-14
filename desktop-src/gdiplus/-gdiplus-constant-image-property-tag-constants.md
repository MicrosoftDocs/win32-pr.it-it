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
# <a name="image-property-tag-constants"></a><span data-ttu-id="42497-103">Costanti Tag proprietà immagine</span><span class="sxs-lookup"><span data-stu-id="42497-103">Image Property Tag Constants</span></span>

<span data-ttu-id="42497-104">Diversi formati di file di immagine consentono di archiviare i metadati insieme a un'immagine.</span><span class="sxs-lookup"><span data-stu-id="42497-104">Several image file formats enable you to store metadata along with an image.</span></span> <span data-ttu-id="42497-105">I metadati sono informazioni su un'immagine, ad esempio titolo, larghezza, modello di fotocamera e artista.</span><span class="sxs-lookup"><span data-stu-id="42497-105">Metadata is information about an image, for example, title, width, camera model, and artist.</span></span> <span data-ttu-id="42497-106">Windows GDI+ fornisce un modo uniforme per archiviare e recuperare i metadati dai file di immagine nei formati Tagged Image File Format (TIFF), JPEG, Portable Network Graphics (PNG) e file di immagine scambiabile (EXIF).</span><span class="sxs-lookup"><span data-stu-id="42497-106">Windows GDI+ provides a uniform way of storing and retrieving metadata from image files in the Tagged Image File Format (TIFF), JPEG, Portable Network Graphics (PNG), and Exchangeable Image File (EXIF) formats.</span></span>

<span data-ttu-id="42497-107">In GDI+, una parte di metadati viene chiamata *elemento della proprietà* e un singolo elemento di proprietà viene identificato da una costante numerica denominata *tag di proprietà*.</span><span class="sxs-lookup"><span data-stu-id="42497-107">In GDI+, a piece of metadata is called a *property item*, and an individual property item is identified by a numerical constant called a *property tag*.</span></span> <span data-ttu-id="42497-108">È possibile archiviare e recuperare i metadati chiamando i metodi [**Image:: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) e [**Image:: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) della classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e non è necessario preoccuparsi dei dettagli relativi all'archiviazione dei metadati in un formato di file specifico.</span><span class="sxs-lookup"><span data-stu-id="42497-108">You can store and retrieve metadata by calling the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) and [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned with the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="42497-109">Negli argomenti seguenti vengono elencati e descritti gli elementi della proprietà supportati da GDI+.</span><span class="sxs-lookup"><span data-stu-id="42497-109">The following topics list and describe the property items supported by GDI+.</span></span> <span data-ttu-id="42497-110">Le descrizioni sono brevi e generali in modo da essere valide per diversi formati di file.</span><span class="sxs-lookup"><span data-stu-id="42497-110">The descriptions are brief and general so that they apply to a variety of file formats.</span></span> <span data-ttu-id="42497-111">Per una descrizione dettagliata della modalità di utilizzo di un elemento di proprietà in un formato di file specifico, vedere la specifica del formato di file.</span><span class="sxs-lookup"><span data-stu-id="42497-111">For a detailed description of how a property item is used in a particular file format, see the specification for that file format.</span></span> <span data-ttu-id="42497-112">Per i collegamenti a diverse specifiche del formato di file, vedere [specifiche del formato del file di immagine](-gdiplus-constant-image-file-format-specifications.md).</span><span class="sxs-lookup"><span data-stu-id="42497-112">For links to several file format specifications, see [Image File Format Specifications](-gdiplus-constant-image-file-format-specifications.md).</span></span> <span data-ttu-id="42497-113">Per ulteriori informazioni sui metadati, vedere la pagina relativa alla [lettura e scrittura](-gdiplus-reading-and-writing-metadata-use.md) di [**costanti di tipo di tag di proprietà Image**](-gdiplus-constant-image-property-tag-type-constants.md)e di metadati.</span><span class="sxs-lookup"><span data-stu-id="42497-113">For more information about metadata, see [Reading and Writing Metadata](-gdiplus-reading-and-writing-metadata-use.md) and [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span>

-   [<span data-ttu-id="42497-114">Tag di proprietà in ordine numerico</span><span class="sxs-lookup"><span data-stu-id="42497-114">Property Tags in Numerical Order</span></span>](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [<span data-ttu-id="42497-115">Tag di proprietà in ordine alfabetico</span><span class="sxs-lookup"><span data-stu-id="42497-115">Property Tags in Alphabetical Order</span></span>](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [<span data-ttu-id="42497-116">Descrizioni degli elementi delle proprietà</span><span class="sxs-lookup"><span data-stu-id="42497-116">Property Item Descriptions</span></span>](-gdiplus-constant-property-item-descriptions.md)

 

 



