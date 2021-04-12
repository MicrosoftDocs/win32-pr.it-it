---
title: Effetto Unpremultiply
description: Utilizzare questo effetto per convertire un'immagine da alfa premoltiplicato a unpremultiplied alfa.
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- effetto unpremultiply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5628ea646443a08abffa4549ad25147deb609acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400825"
---
# <a name="unpremultiply-effect"></a><span data-ttu-id="12bda-104">Effetto Unpremultiply</span><span class="sxs-lookup"><span data-stu-id="12bda-104">Unpremultiply effect</span></span>

<span data-ttu-id="12bda-105">Utilizzare questo effetto per convertire un'immagine da alfa premoltiplicato a unpremultiplied alfa.</span><span class="sxs-lookup"><span data-stu-id="12bda-105">Use this effect to convert an image from premultiplied alpha to unpremultiplied alpha.</span></span> <span data-ttu-id="12bda-106">L'effetto sostituisce ogni pixel di input `P = {R, G, B, A}` con `P' = {R/A, G/A, B/A, A}` nell'output.</span><span class="sxs-lookup"><span data-stu-id="12bda-106">The effect replaces each input pixel `P = {R, G, B, A}` with `P' = {R/A, G/A, B/A, A}` in the output.</span></span>

<span data-ttu-id="12bda-107">Questo effetto non ha proprietà.</span><span class="sxs-lookup"><span data-stu-id="12bda-107">This effect has no properties.</span></span>

<span data-ttu-id="12bda-108">Il CLSID per questo effetto è CLSID \_ D2D1Unpremultiply.</span><span class="sxs-lookup"><span data-stu-id="12bda-108">The CLSID for this effect is CLSID\_D2D1Unpremultiply.</span></span>

## <a name="output-bitmap"></a><span data-ttu-id="12bda-109">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="12bda-109">Output bitmap</span></span>

<span data-ttu-id="12bda-110">La dimensione bitmap di output corrisponde alla dimensione bitmap di input.</span><span class="sxs-lookup"><span data-stu-id="12bda-110">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="12bda-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12bda-111">Requirements</span></span>



| <span data-ttu-id="12bda-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="12bda-112">Requirement</span></span> | <span data-ttu-id="12bda-113">Valore</span><span class="sxs-lookup"><span data-stu-id="12bda-113">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="12bda-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12bda-114">Minimum supported client</span></span> | <span data-ttu-id="12bda-115">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="12bda-115">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="12bda-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12bda-116">Minimum supported server</span></span> | <span data-ttu-id="12bda-117">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="12bda-117">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="12bda-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12bda-118">Header</span></span>                   | <span data-ttu-id="12bda-119">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="12bda-119">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="12bda-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="12bda-120">Library</span></span>                  | <span data-ttu-id="12bda-121">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="12bda-121">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="12bda-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="12bda-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12bda-123">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="12bda-123">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
