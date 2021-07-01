---
description: La fusione alfa viene usata per visualizzare una bitmap alfa, ovvero una bitmap con pixel trasparenti o semitrasparenti.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Alpha Blending (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4add2aca8ac4e2d7e1b24988eb5d40f80bac259c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120286"
---
# <a name="alpha-blending-windows-gdi"></a><span data-ttu-id="b7697-103">Alpha Blending (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="b7697-103">Alpha Blending (Windows GDI)</span></span>

<span data-ttu-id="b7697-104">*La fusione alfa* viene usata per visualizzare una bitmap alfa, ovvero una bitmap con pixel trasparenti o semitrasparenti.</span><span class="sxs-lookup"><span data-stu-id="b7697-104">*Alpha blending* is used to display an alpha bitmap, which is a bitmap that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="b7697-105">Oltre a un canale di colori rosso, verde e blu, ogni pixel in una bitmap alfa ha un componente di trasparenza noto come *canale alfa.*</span><span class="sxs-lookup"><span data-stu-id="b7697-105">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its *alpha channel*.</span></span> <span data-ttu-id="b7697-106">Il canale alfa contiene in genere tutti i bit di un canale di colore.</span><span class="sxs-lookup"><span data-stu-id="b7697-106">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="b7697-107">Ad esempio, un canale alfa a 8 bit può rappresentare 256 livelli di trasparenza, da 0 (l'intera bitmap è trasparente) a 255 (l'intera bitmap è opaca).</span><span class="sxs-lookup"><span data-stu-id="b7697-107">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire bitmap is transparent) to 255 (the entire bitmap is opaque).</span></span>

<span data-ttu-id="b7697-108">I meccanismi di fusione alfa vengono richiamati chiamando [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), che fa riferimento alla [**struttura BLENDFUNCTION.**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction)</span><span class="sxs-lookup"><span data-stu-id="b7697-108">Alpha blending mechanisms are invoked by calling [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), which references the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span>

<span data-ttu-id="b7697-109">I valori alfa per pixel sono supportati solo per RGB BI a 32 \_ bpp.</span><span class="sxs-lookup"><span data-stu-id="b7697-109">Alpha values per pixel are only supported for 32-bpp BI\_RGB.</span></span> <span data-ttu-id="b7697-110">Questa formula è definita come:</span><span class="sxs-lookup"><span data-stu-id="b7697-110">This formula is defined as:</span></span>


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



<span data-ttu-id="b7697-111">È rappresentato in memoria come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b7697-111">This is represented in memory as shown in the following table.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="b7697-112">31:24</span><span class="sxs-lookup"><span data-stu-id="b7697-112">31:24</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="b7697-113">23:16</span><span class="sxs-lookup"><span data-stu-id="b7697-113">23:16</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="b7697-114">15:08</span><span class="sxs-lookup"><span data-stu-id="b7697-114">15:08</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="b7697-115">07:00</span><span class="sxs-lookup"><span data-stu-id="b7697-115">07:00</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="b7697-116">Alfa</span><span class="sxs-lookup"><span data-stu-id="b7697-116">Alpha</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="b7697-117">Red</span><span class="sxs-lookup"><span data-stu-id="b7697-117">Red</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="b7697-118">Green</span><span class="sxs-lookup"><span data-stu-id="b7697-118">Green</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="b7697-119">Blu</span><span class="sxs-lookup"><span data-stu-id="b7697-119">Blue</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="b7697-120">Le bitmap possono anche essere visualizzate con un fattore di trasparenza applicato all'intera bitmap.</span><span class="sxs-lookup"><span data-stu-id="b7697-120">Bitmaps may also be displayed with a transparency factor applied to the entire bitmap.</span></span> <span data-ttu-id="b7697-121">Qualsiasi formato bitmap può essere visualizzato con un valore alfa costante globale impostando **SourceConstantAlpha** nella [**struttura BLENDFUNCTION.**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction)</span><span class="sxs-lookup"><span data-stu-id="b7697-121">Any bitmap format can be displayed with a global constant alpha value by setting **SourceConstantAlpha** in the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span> <span data-ttu-id="b7697-122">Il valore alfa costante globale ha 256 livelli di trasparenza, da 0 (l'intera bitmap è completamente trasparente) a 255 (l'intera bitmap è completamente opaca).</span><span class="sxs-lookup"><span data-stu-id="b7697-122">The global constant alpha value has 256 levels of transparency, from 0 (entire bitmap is completely transparent) to 255 (entire bitmap is completely opaque).</span></span> <span data-ttu-id="b7697-123">Il valore alfa costante globale viene combinato con il valore alfa per pixel.</span><span class="sxs-lookup"><span data-stu-id="b7697-123">The global constant alpha value is combined with the per-pixel alpha value.</span></span>

<span data-ttu-id="b7697-124">Per un esempio, vedere [Alpha Blending a Bitmap (Fusione alfa di una bitmap).](alpha-blending-a-bitmap.md)</span><span class="sxs-lookup"><span data-stu-id="b7697-124">For an example, see [Alpha Blending a Bitmap](alpha-blending-a-bitmap.md).</span></span>

 

 



