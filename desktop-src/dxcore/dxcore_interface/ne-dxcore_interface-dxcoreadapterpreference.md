---
title: DXCoreAdapterPreference
description: Definisce le costanti che specificano le preferenze della scheda DXCore da usare come criteri di ordinamento degli elenchi.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 4301bdc1fe0ece8d9594ec3287e2ea8ddcce8f0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399453"
---
# <a name="dxcoreadapterpreference-enum"></a><span data-ttu-id="29101-103">Enumerazione DXCoreAdapterPreference</span><span class="sxs-lookup"><span data-stu-id="29101-103">DXCoreAdapterPreference enum</span></span>

## <a name="description"></a><span data-ttu-id="29101-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29101-104">Description</span></span>

<span data-ttu-id="29101-105">Definisce le costanti che specificano le preferenze della scheda DXCore da usare come criteri di ordinamento degli elenchi.</span><span class="sxs-lookup"><span data-stu-id="29101-105">Defines constants that specify DXCore adapter preferences to be used as list-sorting criteria.</span></span> <span data-ttu-id="29101-106">È possibile ordinare un elenco di adapter DXCore passando una matrice di **DXCoreAdapterPreference** a [IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span><span class="sxs-lookup"><span data-stu-id="29101-106">You can sort a DXCore adapter list by passing an array of **DXCoreAdapterPreference** to [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="29101-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29101-107">Syntax</span></span>

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a><span data-ttu-id="29101-108">Campi enum</span><span class="sxs-lookup"><span data-stu-id="29101-108">Enum fields</span></span>

### <a name="hardware"></a><span data-ttu-id="29101-109">Hardware</span><span class="sxs-lookup"><span data-stu-id="29101-109">Hardware</span></span>

<span data-ttu-id="29101-110">Specifica una preferenza per le schede hardware (anziché le schede software).</span><span class="sxs-lookup"><span data-stu-id="29101-110">Specifies a preference for hardware adapters (as opposed to software adapters).</span></span>

### <a name="minimumpower"></a><span data-ttu-id="29101-111">MinimumPower</span><span class="sxs-lookup"><span data-stu-id="29101-111">MinimumPower</span></span>

<span data-ttu-id="29101-112">Specifica una preferenza per la GPU a consumo minimo (ad esempio un processore grafico integrato o iGPU).</span><span class="sxs-lookup"><span data-stu-id="29101-112">Specifies a preference for the minimum-powered GPU (such as an integrated graphics processor, or iGPU).</span></span>

### <a name="highperformance"></a><span data-ttu-id="29101-113">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="29101-113">HighPerformance</span></span>

<span data-ttu-id="29101-114">Specifica una preferenza per la GPU con prestazioni più elevate, ad esempio un processore di grafica esterno (xGPU), se disponibile, o dGPU (Discrete Graphics Processor), se disponibile.</span><span class="sxs-lookup"><span data-stu-id="29101-114">Specifies a preference for the highest-performance GPU, such as an external graphics processor (xGPU), if available, or discrete graphics processor (dGPU) if available.</span></span>

## <a name="see-also"></a><span data-ttu-id="29101-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29101-115">See also</span></span>

<span data-ttu-id="29101-116">Riferimento a [IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="29101-116">[IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>