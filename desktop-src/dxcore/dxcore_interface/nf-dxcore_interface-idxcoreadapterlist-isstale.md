---
title: IDXCoreAdapterList::IsStale
description: Determina se le modifiche apportate a questo sistema hanno causato la mancata visualizzazione dell'oggetto elenco di adapter DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68b4e4ba6f3434f76ea5b4a2a98ae4e83486f61e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300376"
---
# <a name="idxcoreadapterlistisstale-method"></a><span data-ttu-id="a896e-103">Metodo IDXCoreAdapterList:: IsValid</span><span class="sxs-lookup"><span data-stu-id="a896e-103">IDXCoreAdapterList::IsStale method</span></span>

<span data-ttu-id="a896e-104">Determina se le modifiche apportate a questo sistema hanno causato la mancata visualizzazione dell'oggetto elenco di adapter DXCore.</span><span class="sxs-lookup"><span data-stu-id="a896e-104">Determines whether changes to this system have resulted in this DXCore adapter list object becoming out of date.</span></span> <span data-ttu-id="a896e-105">Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="a896e-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a896e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a896e-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a><span data-ttu-id="a896e-107">Restituisce</span><span class="sxs-lookup"><span data-stu-id="a896e-107">Returns</span></span>

<span data-ttu-id="a896e-108">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="a896e-108">Type: **bool**</span></span>

<span data-ttu-id="a896e-109">Restituisce  `true`   se, dall'inizio della generazione dell'elenco, sono state apportate modifiche alle condizioni di sistema che potrebbero rendere obsoleto questo elenco di adapter.</span><span class="sxs-lookup"><span data-stu-id="a896e-109">Returns `true` if, since generating the list, changes to system conditions have occurred that would cause this adapter list to become stale.</span></span> <span data-ttu-id="a896e-110">In caso contrario, restituisce  `false` .</span><span class="sxs-lookup"><span data-stu-id="a896e-110">Otherwise, returns `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a896e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a896e-111">Remarks</span></span>

<span data-ttu-id="a896e-112">È possibile eseguire **il polling** per determinare se le condizioni di sistema modificate hanno portato a questo elenco non aggiornato.</span><span class="sxs-lookup"><span data-stu-id="a896e-112">You can poll **IsStale** to determine whether changing system conditions have led to this list becoming out of date.</span></span> <span data-ttu-id="a896e-113">Se il risultato è **obsoleto** `true` , viene restituito `true` per la durata rimanente dell'oggetto elenco di adapter dxcore.</span><span class="sxs-lookup"><span data-stu-id="a896e-113">If **IsStale** returns `true` once, then it returns `true` for the remaining lifetime of the DXCore adapter list object.</span></span> <span data-ttu-id="a896e-114">Un oggetto elenco non aggiornato è ancora considerato obsoleto anche se le condizioni di sistema tornano a uno stato che corrisponde all'elenco (le stesse condizioni ottengono ora come è stato fatto quando l'elenco è stato generato per la prima volta).</span><span class="sxs-lookup"><span data-stu-id="a896e-114">A stale list object is still considered stale even if system conditions return to a state that matches the list (the same conditions obtain now as did when the list was first generated).</span></span>

## <a name="see-also"></a><span data-ttu-id="a896e-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a896e-115">See also</span></span>

<span data-ttu-id="a896e-116">Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="a896e-116">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>