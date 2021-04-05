---
description: Fusione alfa
ms.assetid: 56618e74-32cc-48f8-83b6-4fc31ab6fc36
title: Fusione alfa (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4293448849926cfc6723495619137262e004636e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125208"
---
# <a name="alpha-blending-directshow"></a><span data-ttu-id="4bcf6-103">Fusione alfa (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="4bcf6-103">Alpha Blending (DirectShow)</span></span>

<span data-ttu-id="4bcf6-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="4bcf6-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="4bcf6-105">Questo articolo descrive la fusione alfa in [DirectShow editing Services](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="4bcf6-105">This article describes alpha blending in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="4bcf6-106">Alfa misura la trasparenza di un pixel o di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-106">Alpha measures the transparency of a pixel or image.</span></span> <span data-ttu-id="4bcf6-107">Nel video RGB non compresso a 32 bit, quattro componenti definiscono ogni pixel, ovvero un canale alfa (A) e tre componenti colore (RGB).</span><span class="sxs-lookup"><span data-stu-id="4bcf6-107">In 32-bit uncompressed RGB video, four components define each pixel: an alpha channel (A) and three color components (RGB).</span></span> <span data-ttu-id="4bcf6-108">Un pixel con un valore alfa pari a zero è completamente trasparente.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-108">A pixel with an alpha value of zero is completely transparent.</span></span> <span data-ttu-id="4bcf6-109">Un pixel con un valore alfa pari a 255 è opaco.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-109">A pixel with an alpha value of 255 is opaque.</span></span> <span data-ttu-id="4bcf6-110">Tra questi valori, il pixel presenta diversi gradi di trasparenza.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-110">Between these values, the pixel has various degrees of transparency.</span></span>

<span data-ttu-id="4bcf6-111">DirectShow definisce due tipi di supporto per video RGB a 32 bit:</span><span class="sxs-lookup"><span data-stu-id="4bcf6-111">DirectShow defines two media types for 32-bit RGB video:</span></span>

-   <span data-ttu-id="4bcf6-112">**MEDIASUBTYPE \_ ARGB32**: il video è di 32 bit RGB con un canale alfa valido.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-112">**MEDIASUBTYPE\_ARGB32**: The video is 32-bit RGB with a valid alpha channel.</span></span>
-   <span data-ttu-id="4bcf6-113">**MEDIASUBTYPE \_ RGB32**: i pixel sono 32 bit, ma il canale alfa non è necessariamente valido.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-113">**MEDIASUBTYPE\_RGB32**: Pixels are 32 bits, but the alpha channel is not necessarily valid.</span></span>

<span data-ttu-id="4bcf6-114">Per eseguire la fusione alfa in DES, impostare il tipo di supporto non compresso del gruppo video su MEDIASUBTYPE \_ ARGB32.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-114">To perform alpha blending in DES, set the video group's uncompressed media type to MEDIASUBTYPE\_ARGB32.</span></span> <span data-ttu-id="4bcf6-115">In C++ chiamare il metodo [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="4bcf6-115">In C++, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method.</span></span> <span data-ttu-id="4bcf6-116">Nel formato XTL impostare anche l'attributo [**bitdepth**](bitdepth-attribute.md) dell'elemento [**Group**](group-element.md) su 32.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-116">In the XTL format, setting the [**bitdepth**](bitdepth-attribute.md) attribute of the [**group**](group-element.md) element to 32 accomplishes this as well.</span></span>

<span data-ttu-id="4bcf6-117">Sono quindi necessari dati video contenenti un canale alfa.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-117">Next, you need video data that contains an alpha channel.</span></span> <span data-ttu-id="4bcf6-118">Sono disponibili diverse opzioni:</span><span class="sxs-lookup"><span data-stu-id="4bcf6-118">There are several options:</span></span>

-   <span data-ttu-id="4bcf6-119">È possibile usare un file AVI che ha già un video RGB a 32 bit con dati Alpha.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-119">You can use an AVI file that already has 32-bit RGB video with alpha data.</span></span> <span data-ttu-id="4bcf6-120">Attualmente, Alpha non è supportato per i file di origine MPEG o Microsoft Windows Media Format (WMF).</span><span class="sxs-lookup"><span data-stu-id="4bcf6-120">Currently, alpha is not supported for MPEG or Microsoft Windows Media Format (WMF) source files.</span></span>
-   <span data-ttu-id="4bcf6-121">DES supporta i file di bitmap a 32 bit (BMP) e targa (. tga) con dati alfa.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-121">DES supports 32-bit bitmap (.bmp) and Targa (.tga) files with alpha data.</span></span>
-   <span data-ttu-id="4bcf6-122">È possibile scrivere un filtro di origine personalizzato che crea dati RGB a 32 bit con Alpha.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-122">You can write a custom source filter that creates 32-bit RGB data with alpha.</span></span> <span data-ttu-id="4bcf6-123">Il tipo di supporto di output deve essere **MEDIASUBTYPE \_ ARGB32**.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-123">The output media type must be **MEDIASUBTYPE\_ARGB32**.</span></span> <span data-ttu-id="4bcf6-124">Usare il filtro come sottooggetto in un oggetto di origine della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-124">Use the filter as the subobject in a timeline source object.</span></span>

<span data-ttu-id="4bcf6-125">Se l'origine video non dispone di alfa, è possibile usare un effetto che consente di creare dati alfa.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-125">If your video source does not have alpha, you can use an effect that creates alpha data.</span></span> <span data-ttu-id="4bcf6-126">L' [effetto Alpha Setter](alpha-setter-effect.md) imposta il canale alfa per l'intera immagine su un valore costante.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-126">The [Alpha Setter Effect](alpha-setter-effect.md) sets the alpha channel for the entire image to a constant value.</span></span> <span data-ttu-id="4bcf6-127">Per variare l'alfa nel tempo, usare l'interfaccia [**IPropertySetter**](ipropertysetter.md) con l'effetto di Setter alfa.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-127">To vary the alpha over time, use the [**IPropertySetter**](ipropertysetter.md) interface with the Alpha Setter Effect.</span></span> <span data-ttu-id="4bcf6-128">Non è necessario che l'origine originale sia 32 bit, purché il tipo di supporto non compresso del gruppo sia **MEDIASUBTYPE \_ ARGB32**.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-128">The original source does not have to be 32 bits, as long as the group's uncompressed media type is **MEDIASUBTYPE\_ARGB32**.</span></span>

<span data-ttu-id="4bcf6-129">Infine, passare il video a un effetto o una transizione che esegue la fusione alfa.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-129">Finally, pass the video to an effect or transition that performs alpha blending.</span></span> <span data-ttu-id="4bcf6-130">La [transizione del Compositor](compositor-transition.md) esegue la fusione alfa e la [transizione della chiave](key-transition.md) può essere chiave in base al valore alfa.</span><span class="sxs-lookup"><span data-stu-id="4bcf6-130">The [Compositor Transition](compositor-transition.md) performs alpha blending, and the [Key Transition](key-transition.md) can key by alpha value.</span></span>

<span data-ttu-id="4bcf6-131">Il progetto XTL di esempio seguente esegue la fusione alfa:</span><span class="sxs-lookup"><span data-stu-id="4bcf6-131">The following sample XTL project performs alpha blending:</span></span>


```C++
<timeline>
<group type="video" bitdepth="32" width="320" height="240">
<track>
  <clip start="0" stop="6" src="c:\Example.avi" />
</track>
<track>
  <clip start="0" stop="6" src="c:\Example2.avi">
    <!-- Alpha Setter effect. -->
    <effect clsid="{506D89AE-909A-44f7-9444-ABD575896E35}" start="0" stop="6">
      <param name="alpha" value="255">
        <linear time="6" value="0" />
      </param>
    </effect>
  </clip>
  <!-- Key transition, with alpha keying. -->
  <transition clsid="{C5B19592-145E-11d3-9F04-006008039E37}" start="0" stop="6">
    <param name="KeyType" value="3" />  
  </transition>
</track>
</group>
</timeline>
```



## <a name="related-topics"></a><span data-ttu-id="4bcf6-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4bcf6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bcf6-133">Uso dei servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="4bcf6-133">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



