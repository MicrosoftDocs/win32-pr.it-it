---
title: Punteggi hit testing tocco
description: Le costanti seguenti identificano i possibili punteggi di hit test per un oggetto, rispetto ad altri oggetti che intersecano l'area di contatto tocco.
ms.assetid: EACDE6DB-ADBD-4F0C-8C31-7321AB6A73EA
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_PROXIMITY_CLOSEST
- TOUCH_HIT_TESTING_PROXIMITY_FARTHEST
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: f6590e7d56c1c9d92f0ff20524b6e4222d8655b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517619"
---
# <a name="touch-hit-testing-scores"></a><span data-ttu-id="505ec-103">Punteggi hit testing tocco</span><span class="sxs-lookup"><span data-stu-id="505ec-103">Touch Hit Testing Scores</span></span>

<span data-ttu-id="505ec-104">Le costanti seguenti identificano i possibili punteggi di hit test per un oggetto, rispetto ad altri oggetti che intersecano l'area di contatto tocco.</span><span class="sxs-lookup"><span data-stu-id="505ec-104">The following constants identify the possible hit test scores for an object, relative to other objects that intersect the touch contact area.</span></span>

| <span data-ttu-id="505ec-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="505ec-105">Constant/value</span></span> | <span data-ttu-id="505ec-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="505ec-106">Description</span></span> |
|---|---|
| <span data-ttu-id="505ec-107">**TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0</span><span class="sxs-lookup"><span data-stu-id="505ec-107">**TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0</span></span>      | <span data-ttu-id="505ec-108">L'oggetto è la destinazione più probabile.</span><span class="sxs-lookup"><span data-stu-id="505ec-108">The object is the most probable target.</span></span><br/>  |
| <span data-ttu-id="505ec-109">**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF</span><span class="sxs-lookup"><span data-stu-id="505ec-109">**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF</span></span> | <span data-ttu-id="505ec-110">L'oggetto è la destinazione meno probabile.</span><span class="sxs-lookup"><span data-stu-id="505ec-110">The object is the least probable target.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="505ec-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="505ec-111">Requirements</span></span>

| <span data-ttu-id="505ec-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="505ec-112">Requirement</span></span> | <span data-ttu-id="505ec-113">Valore</span><span class="sxs-lookup"><span data-stu-id="505ec-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="505ec-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="505ec-114">Minimum supported client</span></span><br/> | <span data-ttu-id="505ec-115">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="505ec-115">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="505ec-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="505ec-116">Minimum supported server</span></span><br/> | <span data-ttu-id="505ec-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="505ec-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="505ec-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="505ec-118">Header</span></span><br/>                   | <span data-ttu-id="505ec-119">Winuser. h</span><span class="sxs-lookup"><span data-stu-id="505ec-119">Winuser.h</span></span> |
