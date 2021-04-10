---
title: Effetto premoltiplicato
description: Utilizzare questo effetto per convertire un'immagine da unpremultiplied alfa a alfa premoltiplicato.
ms.assetid: 8A5F55C6-3AC7-48B4-87D8-C19D8B4EA0DD
keywords:
- effetto premoltiplicato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01a8a9ba005ed688a96254856897b3514f05fd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964536"
---
# <a name="premultiply-effect"></a><span data-ttu-id="89fc0-104">Effetto premoltiplicato</span><span class="sxs-lookup"><span data-stu-id="89fc0-104">Premultiply effect</span></span>

<span data-ttu-id="89fc0-105">Utilizzare questo effetto per convertire un'immagine da unpremultiplied alfa a alfa premoltiplicato.</span><span class="sxs-lookup"><span data-stu-id="89fc0-105">Use this effect to convert an image from unpremultiplied alpha to premultiplied alpha.</span></span> <span data-ttu-id="89fc0-106">L'effetto sostituisce ogni pixel di input `P = {R, G, B, A}` con `P' = {R*A, G*A, B*A, A}` nell'output.</span><span class="sxs-lookup"><span data-stu-id="89fc0-106">The effect replaces each input pixel `P = {R, G, B, A}` with `P' = {R*A, G*A, B*A, A}` in the output.</span></span>

<span data-ttu-id="89fc0-107">Questo effetto non ha proprietà.</span><span class="sxs-lookup"><span data-stu-id="89fc0-107">This effect has no properties.</span></span>

<span data-ttu-id="89fc0-108">Il CLSID per questo effetto è CLSID \_ D2D1Premultiply.</span><span class="sxs-lookup"><span data-stu-id="89fc0-108">The CLSID for this effect is CLSID\_D2D1Premultiply.</span></span>

## <a name="output-bitmap"></a><span data-ttu-id="89fc0-109">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="89fc0-109">Output bitmap</span></span>

<span data-ttu-id="89fc0-110">La dimensione bitmap di output corrisponde alla dimensione bitmap di input.</span><span class="sxs-lookup"><span data-stu-id="89fc0-110">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="89fc0-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89fc0-111">Requirements</span></span>



| <span data-ttu-id="89fc0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="89fc0-112">Requirement</span></span> | <span data-ttu-id="89fc0-113">Valore</span><span class="sxs-lookup"><span data-stu-id="89fc0-113">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89fc0-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89fc0-114">Minimum supported client</span></span> | <span data-ttu-id="89fc0-115">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="89fc0-115">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="89fc0-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89fc0-116">Minimum supported server</span></span> | <span data-ttu-id="89fc0-117">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="89fc0-117">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="89fc0-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89fc0-118">Header</span></span>                   | <span data-ttu-id="89fc0-119">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="89fc0-119">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="89fc0-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="89fc0-120">Library</span></span>                  | <span data-ttu-id="89fc0-121">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="89fc0-121">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="89fc0-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89fc0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89fc0-123">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="89fc0-123">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
