---
description: L'attributo stretchmode specifica come estendere un'immagine che non corrisponde alle dimensioni di output.
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: Attributo stretchmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a629a34dc1875a7f1d3669e32c53d0e8d3d29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883729"
---
# <a name="stretchmode-attribute"></a><span data-ttu-id="6d7fb-103">Attributo stretchmode</span><span class="sxs-lookup"><span data-stu-id="6d7fb-103">stretchmode Attribute</span></span>

> [!Note]  
> <span data-ttu-id="6d7fb-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="6d7fb-104">\[Deprecated.</span></span> <span data-ttu-id="6d7fb-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6d7fb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6d7fb-106">L' `stretchmode` attributo specifica come estendere un'immagine che non corrisponde alle dimensioni di output.</span><span class="sxs-lookup"><span data-stu-id="6d7fb-106">The `stretchmode` attribute specifies how to stretch an image that does not match the output dimensions.</span></span>

## <a name="possible-values"></a><span data-ttu-id="6d7fb-107">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="6d7fb-107">Possible Values</span></span>

<span data-ttu-id="6d7fb-108">Deve avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6d7fb-108">Must have one of the following values.</span></span>

-   <span data-ttu-id="6d7fb-109">"Stretch": l'immagine viene adattata alle dimensioni del frame di output senza mantenere le proporzioni.</span><span class="sxs-lookup"><span data-stu-id="6d7fb-109">"stretch": The image is stretched to fit the output frame size without preserving aspect ratio.</span></span> <span data-ttu-id="6d7fb-110">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="6d7fb-110">(Default)</span></span>
-   <span data-ttu-id="6d7fb-111">"Crop": l'immagine viene ritagliata per adattarsi alle dimensioni del frame di output.</span><span class="sxs-lookup"><span data-stu-id="6d7fb-111">"crop": The image is cropped to fit the output frame size.</span></span>
-   <span data-ttu-id="6d7fb-112">"PreserveAspectRatio": le proporzioni originali vengono mantenute, con una letterbox nera lungo la dimensione più breve.</span><span class="sxs-lookup"><span data-stu-id="6d7fb-112">"preserveaspectratio": The original aspect ratio is preserved, with a black letterbox along the shorter dimension.</span></span>
-   <span data-ttu-id="6d7fb-113">"preserveaspectrationoletterbox": l'immagine viene ridimensionata per riempire l'intero frame di destinazione mantenendo le proporzioni.</span><span class="sxs-lookup"><span data-stu-id="6d7fb-113">"preserveaspectrationoletterbox": The image is resized to fill the entire target frame while preserving the aspect ratio.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6d7fb-114">Si applica a</span><span class="sxs-lookup"><span data-stu-id="6d7fb-114">Applies To</span></span>

[<span data-ttu-id="6d7fb-115">**clip**</span><span class="sxs-lookup"><span data-stu-id="6d7fb-115">**clip**</span></span>](clip-element.md)

## <a name="see-also"></a><span data-ttu-id="6d7fb-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d7fb-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d7fb-117">Attributi XTL</span><span class="sxs-lookup"><span data-stu-id="6d7fb-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="6d7fb-118">**IAMTimelineSrc::SetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="6d7fb-118">**IAMTimelineSrc::SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



