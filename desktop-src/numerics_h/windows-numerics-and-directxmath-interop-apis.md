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
# <a name="windows-numerics-and-directxmath-interop-apis"></a>Windows Numerics e API di interoperabilità DirectXMath

Queste funzioni convertono i tipi [**Windows. Foundation. Numerics**](/uwp/api/Windows.Foundation.Numerics) da e verso i tipi DirectXMath SIMD [XMVECTOR](../dxmath/xmvector-data-type.md) e [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).

## <a name="functions"></a>Funzioni

| Nome | Descrizione |
|-|-|
| `XMVECTOR XMLoadFloat2(_In_ float2 const* pSource)` | Carica un float2 in un [XMVECTOR](../dxmath/xmvector-data-type.md)DirectXMath. |
| `XMVECTOR XMLoadFloat3(_In_ float3 const* pSource)` | Carica un float3 in un [XMVECTOR](../dxmath/xmvector-data-type.md)DirectXMath. |
| `XMVECTOR XMLoadFloat4(_In_ float4 const* pSource)` | Carica un float4 in un [XMVECTOR](../dxmath/xmvector-data-type.md)DirectXMath. |
| `XMMATRIX XMLoadFloat3x2(_In_ float3x2 const* pSource)` | Carica un float3x2 in un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath. |
| `XMMATRIX XMLoadFloat4x4(_In_ float4x4 const* pSource)` | Carica un float4x4 in un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath. |
| `XMVECTOR XMLoadPlane(_In_ plane const* pSource)` | Carica un piano in un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath. |
| `XMVECTOR XMLoadQuaternion(_In_ quaternion const* pSource)` | Carica un quaternione in un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath. |
| `void XMStoreFloat2(_Out_ float2* pDestination, _In_ FXMVECTOR value)` | Archivia un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath in un float2. |
| `void XMStoreFloat3(_Out_ float3* pDestination, _In_ FXMVECTOR value)` | Archivia un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath in un float3. |
| `void XMStoreFloat4(_Out_ float4* pDestination, _In_ FXMVECTOR value)` | Archivia un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath in un float4. |
| `void XMStoreFloat3x2(_Out_ float3x2* pDestination, _In_ FXMMATRIX value)` | Archivia un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) DirectXMath in un float3x2. |
| `void XMStoreFloat4x4(_Out_ float4x4* pDestination, _In_ FXMMATRIX value)` | Archivia un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) DirectXMath in un float4x4. |
| `void XMStorePlane(_Out_ plane* pDestination, _In_ FXMVECTOR value)` | Archivia un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath in un piano. |
| `void XMStoreQuaternion(_Out_ quaternion* pDestination, _In_ FXMVECTOR value)` | Archivia un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath in un quaternione. |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Spazio dei nomi | DirectX |
| Intestazione | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[API windowsnumerics. h](windowsnumerics-h-apis-portal.md)
