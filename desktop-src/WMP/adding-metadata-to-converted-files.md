---
title: Aggiunta di metadati ai file convertiti
description: Aggiunta di metadati ai file convertiti
ms.assetid: 97588651-23de-43ab-b884-76d8af95ab93
keywords:
- Media Player Windows, processo di conversione
- Plug-in di Windows Media Player, conversione
- plug-in, conversione
- plug-in di conversione, aggiunta di metadati ai file convertiti
- Aggiunta di metadati ai file convertiti
- metadati, aggiunta ai file convertiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4ae47318089149564f64832c95e4cee1b27f26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727735"
---
# <a name="adding-metadata-to-converted-files"></a><span data-ttu-id="7236f-109">Aggiunta di metadati ai file convertiti</span><span class="sxs-lookup"><span data-stu-id="7236f-109">Adding Metadata to Converted Files</span></span>

<span data-ttu-id="7236f-110">I file convertiti devono contenere determinati metadati per garantire un'esperienza utente ottimale.</span><span class="sxs-lookup"><span data-stu-id="7236f-110">Converted files must contain certain metadata to ensure a good user experience.</span></span> <span data-ttu-id="7236f-111">Come minimo, i file convertiti devono contenere gli attributi primari elencati nelle [linee guida sull'utilizzo dei metadati di Windows Media](/previous-versions/ms867702(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="7236f-111">At a minimum, converted files must contain the primary attributes listed in the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)).</span></span>

<span data-ttu-id="7236f-112">Per file musicali, impostare il valore per **WM/MediaClassPrimaryID** su D1607DBC-E323-4BE2-86A1-48A42A28441E.</span><span class="sxs-lookup"><span data-stu-id="7236f-112">For music files, set the value for **WM/MediaClassPrimaryID** to D1607DBC-E323-4BE2-86A1-48A42A28441E.</span></span>

<span data-ttu-id="7236f-113">Per i file della segreteria telefonica, impostare il valore per **WM/MediaClassPrimaryID** su 01CD0F29-DA4E-4157-897b-6275D50C4F11, ovvero il GUID della classe primaria per i file audio.</span><span class="sxs-lookup"><span data-stu-id="7236f-113">For voicemail files, set the value for **WM/MediaClassPrimaryID** to 01CD0F29-DA4E-4157-897B-6275D50C4F11, which is the primary class GUID for audio files.</span></span> <span data-ttu-id="7236f-114">Impostare il valore per **WM/MediaClassSecondaryID** su 193c8824-4D52-4178-90bd-305240b04636.</span><span class="sxs-lookup"><span data-stu-id="7236f-114">Set the value for **WM/MediaClassSecondaryID** to 193c8824-4d52-4178-90bd-305240b04636.</span></span>

<span data-ttu-id="7236f-115">Per le note vocali, impostare il valore per **WM/MediaClassPrimaryID** su 01CD0F29-DA4E-4157-897b-6275D50C4F11.</span><span class="sxs-lookup"><span data-stu-id="7236f-115">For voice notes, set the value for **WM/MediaClassPrimaryID** to 01CD0F29-DA4E-4157-897B-6275D50C4F11.</span></span> <span data-ttu-id="7236f-116">Impostare il valore per **WM/MediaClassSecondaryID** su 3A172A13-2BD9-4831-835B-114F6A95943F.</span><span class="sxs-lookup"><span data-stu-id="7236f-116">Set the value for **WM/MediaClassSecondaryID** to 3A172A13-2BD9-4831-835B-114F6A95943F.</span></span>

<span data-ttu-id="7236f-117">Impostare il valore per **WM/contentdistributor** sul nome della chiave per il servizio Music che ha fornito il contenuto.</span><span class="sxs-lookup"><span data-stu-id="7236f-117">Set the value for **WM/ContentDistributor** to the key name for the music service that provided the content.</span></span>

<span data-ttu-id="7236f-118">Impostare il valore per **WM/UniqueFileIdentifier** sull'ID contenuto.</span><span class="sxs-lookup"><span data-stu-id="7236f-118">Set the value for **WM/UniqueFileIdentifier** to the content ID.</span></span> <span data-ttu-id="7236f-119">Ciò consentirà di recuperare elementi di contenuto specifici in un momento successivo.</span><span class="sxs-lookup"><span data-stu-id="7236f-119">This will enable you to retrieve specific content items at a future time.</span></span>

<span data-ttu-id="7236f-120">Impostare un valore per **WM/WMShadowFileSourceFileType**.</span><span class="sxs-lookup"><span data-stu-id="7236f-120">Set a value for **WM/WMShadowFileSourceFileType**.</span></span>

<span data-ttu-id="7236f-121">Per il contenuto protetto, usare Windows Media Format SDK per impostare l'attributo **DRM \_ DRMHeader \_ ContentID** sull'ID contenuto.</span><span class="sxs-lookup"><span data-stu-id="7236f-121">For protected content, use the Windows Media Format SDK to set the **DRM\_DRMHeader\_ContentID** attribute to the content ID.</span></span>

<span data-ttu-id="7236f-122">Per contenuto protetto, impostare un valore per **WM/WMShadowFileSourceDRMType**.</span><span class="sxs-lookup"><span data-stu-id="7236f-122">For protected content, set a value for **WM/WMShadowFileSourceDRMType**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7236f-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7236f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7236f-124">**Informazioni sui plug-in di conversione**</span><span class="sxs-lookup"><span data-stu-id="7236f-124">**About Conversion Plug-ins**</span></span>](about-conversion-plug-ins.md)
</dt> <dt>

[<span data-ttu-id="7236f-125">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="7236f-125">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 