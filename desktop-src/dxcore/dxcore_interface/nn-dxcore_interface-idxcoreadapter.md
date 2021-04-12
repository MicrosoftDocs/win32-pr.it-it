---
title: IDXCoreAdapter
description: L' ****   interfaccia IDXCoreAdapter implementa i metodi per il recupero dei dettagli relativi a un elemento adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0930ce76353d556f7839f476ec8979823eac3a6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118303"
---
# <a name="idxcoreadapter-interface"></a><span data-ttu-id="45a44-103">Interfaccia IDXCoreAdapter</span><span class="sxs-lookup"><span data-stu-id="45a44-103">IDXCoreAdapter interface</span></span>

<span data-ttu-id="45a44-104">L' \*\*\*\*   interfaccia IDXCoreAdapter implementa i metodi per il recupero dei dettagli relativi a un elemento adapter.</span><span class="sxs-lookup"><span data-stu-id="45a44-104">The **IDXCoreAdapter** interface implements methods for retrieving details about an adapter item.</span></span> <span data-ttu-id="45a44-105">**IDXCoreAdapter** eredita dall'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="45a44-105">**IDXCoreAdapter** inherits from the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="45a44-106">Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="45a44-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="45a44-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="45a44-107">Remarks</span></span>

<span data-ttu-id="45a44-108">Le proprietà di un adapter vengono stabilite nel momento in cui l'adapter viene avviato e non sono modificabili per la durata dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="45a44-108">An adapter's properties are established at the time the adapter starts, and they're immutable for the lifetime of the adapter.</span></span> <span data-ttu-id="45a44-109">Questo si differenzia dallo stato di un adapter, che può essere sottoposto a query o impostato, e i cui valori possono cambiare nel tempo.</span><span class="sxs-lookup"><span data-stu-id="45a44-109">This is in contrast to an adapter's state, which can be queried or set, and the values of which can change over time.</span></span>

## <a name="see-also"></a><span data-ttu-id="45a44-110">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45a44-110">See also</span></span>

<span data-ttu-id="45a44-111">Guida di [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="45a44-111">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>