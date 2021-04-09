---
title: IDXCoreAdapter::IsQueryStateSupported
description: Determina se questo oggetto adapter DXCore e il sistema operativo corrente supportano l'esecuzione di query sul valore dello stato dell'adapter specificato.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: d154597f9b3ddbec24cff230317d881b9595bcde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118151"
---
# <a name="idxcoreadapterisquerystatesupported-method"></a><span data-ttu-id="206b6-103">Metodo IDXCoreAdapter:: IsQueryStateSupported</span><span class="sxs-lookup"><span data-stu-id="206b6-103">IDXCoreAdapter::IsQueryStateSupported method</span></span>

<span data-ttu-id="206b6-104">Determina se questo oggetto adapter DXCore e il sistema operativo corrente supportano l'esecuzione di query sul valore dello stato dell'adapter specificato.</span><span class="sxs-lookup"><span data-stu-id="206b6-104">Determines whether this DXCore adapter object and the current operating system (OS) support querying the value of the specified adapter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="206b6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="206b6-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsQueryStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a><span data-ttu-id="206b6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="206b6-106">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="206b6-107">state</span><span class="sxs-lookup"><span data-stu-id="206b6-107">state</span></span>

<span data-ttu-id="206b6-108">Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="206b6-108">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="206b6-109">Tipo di elemento di stato su cui si sta eseguendo una query sul supporto per.</span><span class="sxs-lookup"><span data-stu-id="206b6-109">The kind of state item that you're querying about support for.</span></span> <span data-ttu-id="206b6-110">Per ulteriori informazioni su ogni tipo di stato dell'adapter, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="206b6-110">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="206b6-111">Restituisce</span><span class="sxs-lookup"><span data-stu-id="206b6-111">Returns</span></span>

<span data-ttu-id="206b6-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="206b6-112">Type: **bool**</span></span>

<span data-ttu-id="206b6-113">Restituisce  `true`   se l'oggetto adattatore DXCore e il sistema operativo corrente supportano l'esecuzione di query sullo stato dell'adapter specificato.</span><span class="sxs-lookup"><span data-stu-id="206b6-113">Returns `true` if this DXCore adapter object and the current operating system (OS) support querying the specified adapter state.</span></span> <span data-ttu-id="206b6-114">In caso contrario, restituisce  `false` .</span><span class="sxs-lookup"><span data-stu-id="206b6-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="206b6-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="206b6-115">See also</span></span>

<span data-ttu-id="206b6-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [riferimento a DXCore](../dxcore-reference.md), [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="206b6-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>