---
title: IDXCoreAdapter::IsAttributeSupported
description: Determina se questo oggetto adapter DXCore supporta l'attributo dell'adattatore specificato.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9824595326f9e81bfa21ab198a3f5b2e6eae74bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399169"
---
# <a name="idxcoreadapterisattributesupported-method"></a><span data-ttu-id="34684-103">Metodo IDXCoreAdapter:: IsAttributeSupported</span><span class="sxs-lookup"><span data-stu-id="34684-103">IDXCoreAdapter::IsAttributeSupported method</span></span>

<span data-ttu-id="34684-104">Determina se questo oggetto adapter DXCore supporta l'attributo dell'adattatore specificato.</span><span class="sxs-lookup"><span data-stu-id="34684-104">Determines whether this DXCore adapter object supports the specified adapter attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="34684-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34684-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a><span data-ttu-id="34684-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="34684-106">Parameters</span></span>

### <a name="attributeguid"></a><span data-ttu-id="34684-107">attributeGUID</span><span class="sxs-lookup"><span data-stu-id="34684-107">attributeGUID</span></span>

<span data-ttu-id="34684-108">Tipo: **REFGUID**</span><span class="sxs-lookup"><span data-stu-id="34684-108">Type: **REFGUID**</span></span>

<span data-ttu-id="34684-109">Riferimento a un GUID dell'attributo dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="34684-109">A reference to an adapter attribute GUID.</span></span> <span data-ttu-id="34684-110">Per un elenco di GUID di attributo, vedere i [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md).</span><span class="sxs-lookup"><span data-stu-id="34684-110">For a list of attribute GUIDs, see [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md).</span></span>

## <a name="returns"></a><span data-ttu-id="34684-111">Restituisce</span><span class="sxs-lookup"><span data-stu-id="34684-111">Returns</span></span>

<span data-ttu-id="34684-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="34684-112">Type: **bool**</span></span>

<span data-ttu-id="34684-113">Restituisce  `true`   se l'oggetto adattatore DXCore supporta l'attributo dell'adattatore specificato.</span><span class="sxs-lookup"><span data-stu-id="34684-113">Returns `true` if this DXCore adapter object supports the specified adapter attribute.</span></span> <span data-ttu-id="34684-114">In caso contrario, restituisce  `false` .</span><span class="sxs-lookup"><span data-stu-id="34684-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="34684-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34684-115">See also</span></span>

<span data-ttu-id="34684-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [riferimento a DXCore](../dxcore-reference.md), [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="34684-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>