---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Determina se un valore [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) specificato viene riconosciuto dal sistema operativo.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 1678568eb17c0dd833c130e6184931c8896261e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728039"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a><span data-ttu-id="07544-103">Metodo IDXCoreAdapterList:: IsAdapterPreferenceSupported</span><span class="sxs-lookup"><span data-stu-id="07544-103">IDXCoreAdapterList::IsAdapterPreferenceSupported method</span></span>

## <a name="description"></a><span data-ttu-id="07544-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07544-104">Description</span></span>

<span data-ttu-id="07544-105">Determina se un valore [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) specificato viene riconosciuto dal sistema operativo corrente.</span><span class="sxs-lookup"><span data-stu-id="07544-105">Determines whether a specified [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value is understood by the current operating system (OS).</span></span> <span data-ttu-id="07544-106">È possibile chiamare **IsAdapterPreferenceSupported** prima di chiamare [IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span><span class="sxs-lookup"><span data-stu-id="07544-106">You can call **IsAdapterPreferenceSupported** before calling [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="07544-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07544-107">Syntax</span></span>

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a><span data-ttu-id="07544-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="07544-108">Parameters</span></span>

### <a name="preference"></a><span data-ttu-id="07544-109">preference</span><span class="sxs-lookup"><span data-stu-id="07544-109">preference</span></span>

<span data-ttu-id="07544-110">Tipo: **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**</span><span class="sxs-lookup"><span data-stu-id="07544-110">Type: **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**</span></span>

<span data-ttu-id="07544-111">Valore [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) che verrà controllato per verificare se è supportato dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="07544-111">A [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value that will be checked to see whether it's supported by the OS.</span></span>

## <a name="returns"></a><span data-ttu-id="07544-112">Restituisce</span><span class="sxs-lookup"><span data-stu-id="07544-112">Returns</span></span>

<span data-ttu-id="07544-113">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="07544-113">Type: **bool**</span></span>

<span data-ttu-id="07544-114">Restituisce `true` se il tipo di ordinamento viene riconosciuto dal sistema operativo corrente.</span><span class="sxs-lookup"><span data-stu-id="07544-114">Returns `true` if the sort type is understood by the current OS.</span></span> <span data-ttu-id="07544-115">In caso contrario, restituisce `false`.</span><span class="sxs-lookup"><span data-stu-id="07544-115">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="07544-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07544-116">See also</span></span>

<span data-ttu-id="07544-117">Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="07544-117">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>