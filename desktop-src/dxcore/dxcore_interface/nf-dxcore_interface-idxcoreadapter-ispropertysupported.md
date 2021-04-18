---
title: IDXCoreAdapter::IsPropertySupported
description: Determina se questo oggetto adapter DXCore e il sistema operativo corrente supportano la proprietà dell'adapter specificata.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b960d96515d4aee85520a6def70a8f0e9349e131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300218"
---
# <a name="idxcoreadapterispropertysupported-method"></a><span data-ttu-id="f738e-103">Metodo IDXCoreAdapter:: IsPropertySupported</span><span class="sxs-lookup"><span data-stu-id="f738e-103">IDXCoreAdapter::IsPropertySupported method</span></span>

<span data-ttu-id="f738e-104">Determina se questo oggetto adapter DXCore e il sistema operativo corrente supportano la proprietà dell'adapter specificata.</span><span class="sxs-lookup"><span data-stu-id="f738e-104">Determines whether this DXCore adapter object and the current operating system (OS) support the specified adapter property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f738e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f738e-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a><span data-ttu-id="f738e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f738e-106">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="f738e-107">proprietà</span><span class="sxs-lookup"><span data-stu-id="f738e-107">property</span></span>

<span data-ttu-id="f738e-108">Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="f738e-108">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="f738e-109">Tipo di proprietà su cui si sta eseguendo una query sul supporto per.</span><span class="sxs-lookup"><span data-stu-id="f738e-109">The type of property that you're querying about support for.</span></span> <span data-ttu-id="f738e-110">Per ulteriori informazioni su ogni proprietà dell'adapter, vedere la tabella in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="f738e-110">See the table in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) for more info about each adapter property.</span></span>

## <a name="returns"></a><span data-ttu-id="f738e-111">Restituisce</span><span class="sxs-lookup"><span data-stu-id="f738e-111">Returns</span></span>

<span data-ttu-id="f738e-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="f738e-112">Type: **bool**</span></span>

<span data-ttu-id="f738e-113">Restituisce  `true`   se l'oggetto adattatore DXCore e il sistema operativo corrente supportano la proprietà dell'adapter specificata.</span><span class="sxs-lookup"><span data-stu-id="f738e-113">Returns `true` if this DXCore adapter object and the current operating system (OS) support the specified adapter property.</span></span> <span data-ttu-id="f738e-114">In caso contrario, restituisce  `false` .</span><span class="sxs-lookup"><span data-stu-id="f738e-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="f738e-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f738e-115">See also</span></span>

<span data-ttu-id="f738e-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [riferimento a DXCore](../dxcore-reference.md), [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="f738e-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>