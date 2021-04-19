---
title: Windows Numerics e API di interoperabilità DirectXMath (Windowsnumerics. h)
description: Queste funzioni convertono i tipi Windows. Foundation. Numerics da e verso i tipi DirectXMath SIMD XMVECTOR e XMMATRIX.
ms.assetid: 05851054-196E-4955-B9C5-85C2E33EF488
keywords:
- Windows Numerics e API di interoperabilità DirectXMath
topic_type:
- apiref
api_name:
- WWindows numerics and DirectXMath interop APIs
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e39057c92eeed87c3f429acb56f0afa2468ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332788"
---
# <a name="windows-numerics-and-directxmath-interop-apis"></a><span data-ttu-id="52912-104">Windows Numerics e API di interoperabilità DirectXMath</span><span class="sxs-lookup"><span data-stu-id="52912-104">Windows numerics and DirectXMath interop APIs</span></span>

<span data-ttu-id="52912-105">Queste funzioni convertono i tipi [**Windows. Foundation. Numerics**](/uwp/api/Windows.Foundation.Numerics) da e verso i tipi DirectXMath SIMD [XMVECTOR](../dxmath/xmvector-data-type.md) e [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="52912-105">These functions convert [**Windows.Foundation.Numerics**](/uwp/api/Windows.Foundation.Numerics) types to and from the DirectXMath SIMD types [XMVECTOR](../dxmath/xmvector-data-type.md) and [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span>

## <a name="functions"></a><span data-ttu-id="52912-106">Funzioni</span><span class="sxs-lookup"><span data-stu-id="52912-106">Functions</span></span>

| <span data-ttu-id="52912-107">Nome</span><span class="sxs-lookup"><span data-stu-id="52912-107">Name</span></span> | <span data-ttu-id="52912-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52912-108">Description</span></span> |
|-|-|
| `XMVECTOR XMLoadFloat2(_In_ float2 const* pSource)` | <span data-ttu-id="52912-109">Carica un float2 in un [XMVECTOR](../dxmath/xmvector-data-type.md)DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="52912-109">Loads a float2 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMVECTOR XMLoadFloat3(_In_ float3 const* pSource)` | <span data-ttu-id="52912-110">Carica un float3 in un [XMVECTOR](../dxmath/xmvector-data-type.md)DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="52912-110">Loads a float3 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMVECTOR XMLoadFloat4(_In_ float4 const* pSource)` | <span data-ttu-id="52912-111">Carica un float4 in un [XMVECTOR](../dxmath/xmvector-data-type.md)DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="52912-111">Loads a float4 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMMATRIX XMLoadFloat3x2(_In_ float3x2 const* pSource)` | <span data-ttu-id="52912-112">Carica un float3x2 in un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="52912-112">Loads a float3x2 into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMMATRIX XMLoadFloat4x4(_In_ float4x4 const* pSource)` | <span data-ttu-id="52912-113">Carica un float4x4 in un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="52912-113">Loads a float4x4 into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMVECTOR XMLoadPlane(_In_ plane const* pSource)` | <span data-ttu-id="52912-114">Carica un piano in un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="52912-114">Loads a plane into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMVECTOR XMLoadQuaternion(_In_ quaternion const* pSource)` | <span data-ttu-id="52912-115">Carica un quaternione in un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="52912-115">Loads a quaternion into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `void XMStoreFloat2(_Out_ float2* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="52912-116">Archivia un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath in un float2.</span><span class="sxs-lookup"><span data-stu-id="52912-116">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float2.</span></span> |
| `void XMStoreFloat3(_Out_ float3* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="52912-117">Archivia un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath in un float3.</span><span class="sxs-lookup"><span data-stu-id="52912-117">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float3.</span></span> |
| `void XMStoreFloat4(_Out_ float4* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="52912-118">Archivia un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath in un float4.</span><span class="sxs-lookup"><span data-stu-id="52912-118">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float4.</span></span> |
| `void XMStoreFloat3x2(_Out_ float3x2* pDestination, _In_ FXMMATRIX value)` | <span data-ttu-id="52912-119">Archivia un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) DirectXMath in un float3x2.</span><span class="sxs-lookup"><span data-stu-id="52912-119">Stores a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into a float3x2.</span></span> |
| `void XMStoreFloat4x4(_Out_ float4x4* pDestination, _In_ FXMMATRIX value)` | <span data-ttu-id="52912-120">Archivia un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) DirectXMath in un float4x4.</span><span class="sxs-lookup"><span data-stu-id="52912-120">Stores a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into a float4x4.</span></span> |
| `void XMStorePlane(_Out_ plane* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="52912-121">Archivia un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath in un piano.</span><span class="sxs-lookup"><span data-stu-id="52912-121">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a plane.</span></span> |
| `void XMStoreQuaternion(_Out_ quaternion* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="52912-122">Archivia un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath in un quaternione.</span><span class="sxs-lookup"><span data-stu-id="52912-122">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a quaternion.</span></span> |

## <a name="requirements"></a><span data-ttu-id="52912-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52912-123">Requirements</span></span>

| <span data-ttu-id="52912-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="52912-124">Requirement</span></span> | <span data-ttu-id="52912-125">Valore</span><span class="sxs-lookup"><span data-stu-id="52912-125">Value</span></span> |
|-|-|
| <span data-ttu-id="52912-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="52912-126">Namespace</span></span> | <span data-ttu-id="52912-127">DirectX</span><span class="sxs-lookup"><span data-stu-id="52912-127">DirectX</span></span> |
| <span data-ttu-id="52912-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52912-128">Header</span></span> | <dl> <span data-ttu-id="52912-129"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="52912-129"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="52912-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52912-130">See also</span></span>

[<span data-ttu-id="52912-131">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="52912-131">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
