---
description: 'I metodi Image:: Save e i metodi Image:: SaveAdd della classe Image ricevono un oggetto EncoderParameters che contiene una matrice di oggetti EncoderParameter.'
ms.assetid: babc89f0-aea5-4341-8cf9-40d11e73fb10
title: Costanti del codificatore di immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8130b90ad7f1d559ca480a581a0b157ff152fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227092"
---
# <a name="image-encoder-constants"></a><span data-ttu-id="7c0e8-103">Costanti del codificatore di immagini</span><span class="sxs-lookup"><span data-stu-id="7c0e8-103">Image Encoder Constants</span></span>

<span data-ttu-id="7c0e8-104">I metodi [Image:: Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) e i metodi [Image:: SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) della classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) ricevono un oggetto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) che contiene una matrice di oggetti [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="7c0e8-104">The [Image::Save Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) and [Image::SaveAdd Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) methods of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class receive an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object that contains an array of [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects.</span></span> <span data-ttu-id="7c0e8-105">Ogni oggetto **EncoderParameter** dispone di un membro dati GUID che specifica la categoria di parametri.</span><span class="sxs-lookup"><span data-stu-id="7c0e8-105">Each **EncoderParameter** object has a GUID data member that specifies the parameter category.</span></span> <span data-ttu-id="7c0e8-106">Le costanti seguenti, definite in Gdiplusimaging. h, rappresentano i GUID che specificano le varie categorie di parametri.</span><span class="sxs-lookup"><span data-stu-id="7c0e8-106">The following constants, defined in Gdiplusimaging.h, represent GUIDs that specify the various parameter categories.</span></span>

-   <span data-ttu-id="7c0e8-107">EncoderChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="7c0e8-107">EncoderChrominanceTable</span></span>
-   <span data-ttu-id="7c0e8-108">EncoderColorDepth</span><span class="sxs-lookup"><span data-stu-id="7c0e8-108">EncoderColorDepth</span></span>
-   <span data-ttu-id="7c0e8-109">EncoderColorSpace</span><span class="sxs-lookup"><span data-stu-id="7c0e8-109">EncoderColorSpace</span></span>
-   <span data-ttu-id="7c0e8-110">EncoderCompression</span><span class="sxs-lookup"><span data-stu-id="7c0e8-110">EncoderCompression</span></span>
-   <span data-ttu-id="7c0e8-111">EncoderLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="7c0e8-111">EncoderLuminanceTable</span></span>
-   <span data-ttu-id="7c0e8-112">EncoderQuality</span><span class="sxs-lookup"><span data-stu-id="7c0e8-112">EncoderQuality</span></span>
-   <span data-ttu-id="7c0e8-113">EncoderRenderMethod</span><span class="sxs-lookup"><span data-stu-id="7c0e8-113">EncoderRenderMethod</span></span>
-   <span data-ttu-id="7c0e8-114">EncoderSaveFlag</span><span class="sxs-lookup"><span data-stu-id="7c0e8-114">EncoderSaveFlag</span></span>
-   <span data-ttu-id="7c0e8-115">EncoderScanMethod</span><span class="sxs-lookup"><span data-stu-id="7c0e8-115">EncoderScanMethod</span></span>
-   <span data-ttu-id="7c0e8-116">EncoderTransformation</span><span class="sxs-lookup"><span data-stu-id="7c0e8-116">EncoderTransformation</span></span>
-   <span data-ttu-id="7c0e8-117">EncoderVersion</span><span class="sxs-lookup"><span data-stu-id="7c0e8-117">EncoderVersion</span></span>
-   <span data-ttu-id="7c0e8-118">EncoderImageItems</span><span class="sxs-lookup"><span data-stu-id="7c0e8-118">EncoderImageItems</span></span>
-   <span data-ttu-id="7c0e8-119">EncoderSaveAsCMYK</span><span class="sxs-lookup"><span data-stu-id="7c0e8-119">EncoderSaveAsCMYK</span></span>

 

 
