---
title: IDXCoreAdapter::IsSetStateSupported
description: Determina se questo oggetto adattatore DXCore e il sistema operativo corrente supportano l'impostazione del valore dello stato dell'adapter specificato.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 284e38a622c882fce04278d9134908f55c9a25cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399452"
---
# <a name="idxcoreadapterissetstatesupported-method"></a><span data-ttu-id="f1853-103">Metodo IDXCoreAdapter:: IsSetStateSupported</span><span class="sxs-lookup"><span data-stu-id="f1853-103">IDXCoreAdapter::IsSetStateSupported method</span></span>

<span data-ttu-id="f1853-104">Determina se questo oggetto adattatore DXCore e il sistema operativo corrente supportano l'impostazione del valore dello stato dell'adapter specificato.</span><span class="sxs-lookup"><span data-stu-id="f1853-104">Determines whether this DXCore adapter object and the current operating system (OS) support setting the value of the specified adapter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1853-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1853-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsSetStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a><span data-ttu-id="f1853-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1853-106">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="f1853-107">state</span><span class="sxs-lookup"><span data-stu-id="f1853-107">state</span></span>

<span data-ttu-id="f1853-108">Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="f1853-108">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="f1853-109">Tipo di elemento di stato su cui si sta eseguendo una query sul supporto per.</span><span class="sxs-lookup"><span data-stu-id="f1853-109">The kind of state item that you're querying about support for.</span></span> <span data-ttu-id="f1853-110">Per ulteriori informazioni su ogni tipo di stato dell'adapter, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="f1853-110">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="f1853-111">Restituisce</span><span class="sxs-lookup"><span data-stu-id="f1853-111">Returns</span></span>

<span data-ttu-id="f1853-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="f1853-112">Type: **bool**</span></span>

<span data-ttu-id="f1853-113">Restituisce  `true`   se l'oggetto adattatore DXCore e il sistema operativo corrente (sistema operativo) supportano l'impostazione dello stato dell'adapter specificato.</span><span class="sxs-lookup"><span data-stu-id="f1853-113">Returns `true` if this DXCore adapter object and the current operating system (OS) support setting the specified adapter state.</span></span> <span data-ttu-id="f1853-114">In caso contrario, restituisce  `false` .</span><span class="sxs-lookup"><span data-stu-id="f1853-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1853-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1853-115">See also</span></span>

<span data-ttu-id="f1853-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [riferimento a DXCore](../dxcore-reference.md), [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="f1853-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>