---
description: La fusione alfa viene utilizzata per visualizzare una bitmap Alpha, ovvero una bitmap con pixel trasparenti o semitrasparenti.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Fusione alfa (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68cb34d189fb80d23cbb5eeec9d9006aa93a1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978826"
---
# <a name="alpha-blending-windows-gdi"></a><span data-ttu-id="8684a-103">Fusione alfa (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="8684a-103">Alpha Blending (Windows GDI)</span></span>

<span data-ttu-id="8684a-104">La *fusione alfa* viene utilizzata per visualizzare una bitmap Alpha, ovvero una bitmap con pixel trasparenti o semitrasparenti.</span><span class="sxs-lookup"><span data-stu-id="8684a-104">*Alpha blending* is used to display an alpha bitmap, which is a bitmap that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="8684a-105">Oltre a un canale di colore rosso, verde e blu, ogni pixel in una bitmap alfa presenta un componente di trasparenza noto come *canale alfa*.</span><span class="sxs-lookup"><span data-stu-id="8684a-105">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its *alpha channel*.</span></span> <span data-ttu-id="8684a-106">Il canale alfa contiene in genere tutti i bit di un canale colori.</span><span class="sxs-lookup"><span data-stu-id="8684a-106">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="8684a-107">Un canale alfa a 8 bit, ad esempio, può rappresentare 256 livelli di trasparenza, da 0 (l'intera bitmap è trasparente) a 255 (l'intera bitmap è opaca).</span><span class="sxs-lookup"><span data-stu-id="8684a-107">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire bitmap is transparent) to 255 (the entire bitmap is opaque).</span></span>

<span data-ttu-id="8684a-108">I meccanismi di fusione alfa vengono richiamati chiamando [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), che fa riferimento alla struttura [**BlendFunction**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) .</span><span class="sxs-lookup"><span data-stu-id="8684a-108">Alpha blending mechanisms are invoked by calling [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), which references the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span>

<span data-ttu-id="8684a-109">I valori alfa per pixel sono supportati solo per l'RGB BI 32-bpp \_ .</span><span class="sxs-lookup"><span data-stu-id="8684a-109">Alpha values per pixel are only supported for 32-bpp BI\_RGB.</span></span> <span data-ttu-id="8684a-110">Questa formula viene definita come segue:</span><span class="sxs-lookup"><span data-stu-id="8684a-110">This formula is defined as:</span></span>


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



<span data-ttu-id="8684a-111">Questa operazione viene rappresentata in memoria, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8684a-111">This is represented in memory as shown in the following table.</span></span>



|       |       |       |       |
|-------|-------|-------|-------|
| <span data-ttu-id="8684a-112">31:24</span><span class="sxs-lookup"><span data-stu-id="8684a-112">31:24</span></span> | <span data-ttu-id="8684a-113">23:16</span><span class="sxs-lookup"><span data-stu-id="8684a-113">23:16</span></span> | <span data-ttu-id="8684a-114">15:08</span><span class="sxs-lookup"><span data-stu-id="8684a-114">15:08</span></span> | <span data-ttu-id="8684a-115">07:00</span><span class="sxs-lookup"><span data-stu-id="8684a-115">07:00</span></span> |
| <span data-ttu-id="8684a-116">Alfa</span><span class="sxs-lookup"><span data-stu-id="8684a-116">Alpha</span></span> | <span data-ttu-id="8684a-117">Red</span><span class="sxs-lookup"><span data-stu-id="8684a-117">Red</span></span>   | <span data-ttu-id="8684a-118">Green</span><span class="sxs-lookup"><span data-stu-id="8684a-118">Green</span></span> | <span data-ttu-id="8684a-119">Blu</span><span class="sxs-lookup"><span data-stu-id="8684a-119">Blue</span></span>  |



 

<span data-ttu-id="8684a-120">Le bitmap possono essere visualizzate anche con un fattore di trasparenza applicato all'intera bitmap.</span><span class="sxs-lookup"><span data-stu-id="8684a-120">Bitmaps may also be displayed with a transparency factor applied to the entire bitmap.</span></span> <span data-ttu-id="8684a-121">Qualsiasi formato bitmap può essere visualizzato con un valore alfa costante globale impostando **SourceConstantAlpha** nella struttura [**BlendFunction**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) .</span><span class="sxs-lookup"><span data-stu-id="8684a-121">Any bitmap format can be displayed with a global constant alpha value by setting **SourceConstantAlpha** in the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span> <span data-ttu-id="8684a-122">Il valore alfa costante globale presenta 256 livelli di trasparenza, da 0 (intera bitmap completamente trasparente) a 255 (l'intera bitmap è completamente opaca).</span><span class="sxs-lookup"><span data-stu-id="8684a-122">The global constant alpha value has 256 levels of transparency, from 0 (entire bitmap is completely transparent) to 255 (entire bitmap is completely opaque).</span></span> <span data-ttu-id="8684a-123">Il valore alfa della costante globale è combinato con il valore alfa per pixel.</span><span class="sxs-lookup"><span data-stu-id="8684a-123">The global constant alpha value is combined with the per-pixel alpha value.</span></span>

<span data-ttu-id="8684a-124">Per un esempio, vedere [fusione alfa di una bitmap](alpha-blending-a-bitmap.md).</span><span class="sxs-lookup"><span data-stu-id="8684a-124">For an example, see [Alpha Blending a Bitmap](alpha-blending-a-bitmap.md).</span></span>

 

 



