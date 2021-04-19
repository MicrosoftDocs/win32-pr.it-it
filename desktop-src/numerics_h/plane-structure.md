---
title: struttura del piano (Windowsnumerics. h)
description: Questa struttura rappresenta un piano usando un vettore 3D normale e un valore di distanza.
ms.assetid: 3C5A5EA0-8A51-4F9B-A84A-0C8E726CE3FD
keywords:
- struttura del piano
topic_type:
- apiref
api_name:
- plane structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d870e2769121b4aec542235081011406e439d579
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332790"
---
# <a name="plane-structure"></a>struttura del piano

Questa struttura rappresenta un piano usando un vettore 3D normale e un valore di distanza.

Questo tipo è disponibile solo in C++. Il relativo equivalente .NET è [System. Numerics. Plane](/dotnet/api/system.numerics.plane?view=netframework-4.8).

## <a name="constructors"></a>Costruttori

| Nome | Descrizione |
|-|-|
| `plane()` | Crea un piano non inizializzato. |
| `plane(float x, float y, float z, float d)` | Crea un piano con i valori specificati. |
| `plane(float3 normal, float d)` | Crea un piano da un float3 e da una distanza. |
| `explicit plane(float4 value)` | Crea un piano da un float4. |
| `plane(Microsoft::?Graphics::?Canvas::?Numerics::?Plane const& value)` | Converte un oggetto **Microsoft. graphics. Canvas. Numerics. Plane** in un piano. |

## <a name="functions"></a>Funzioni

| Nome | Descrizione |
|-|-|
| `plane make_plane_from_vertices(float3 const& point1, float3 const& point2, float3 const& point3)` | Crea un piano da un set di tre posizioni del vertice, che devono essere tutte diverse e non in una linea retta. |
| `plane normalize(plane const& value)` | Modifica i coefficienti del vettore normale di un piano per renderlo di lunghezza dell'unità. |
| `plane transform(plane const& plane, float4x4 const& matrix)` | Trasforma un piano normalizzato in base a una matrice. |
| `plane transform(plane const& plane, quaternion const& rotation)` | Trasforma un piano normalizzato in base a una rotazione quaternione. |
| `float dot(plane const& plane, float4 const& value)` | Calcola il prodotto a punti di un piano con un vettore. |
| `float dot_coordinate(plane const& plane, float3 const& value)` | Calcola il prodotto punto di un piano con una coordinata float3. Diversamente dal punto \_ normale, questo calcolo include il valore del piano d. |
| `float dot_normal(plane const& plane, float3 const& value)` | Calcola il prodotto a punti di un piano con una normale float3. A differenza \_ della coordinata del punto, questo calcolo ignora il valore del piano d. |

## <a name="operators"></a>Operatori

| Nome | Descrizione |
|-|-|
| `bool operator== (plane const& value1, plane const& value2)` | Determina se due istanze del piano sono uguali. |
| `bool operator!= (plane const& value1, plane const& value2)` | Determina se due istanze del piano non sono uguali. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Plane() const` | Converte un piano in un oggetto **Microsoft. graphics. Canvas. Numerics. Plane**. |

## <a name="fields"></a>Campi

| Nome | Descrizione |
|-|-|
| `float3 normal` | Vettore normale del piano. |
| `float d` | Distanza del piano lungo la normale dall'origine. |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Spazio dei nomi | Windows:: Foundation:: Numerics |
| Intestazione | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[API windowsnumerics. h](windowsnumerics-h-apis-portal.md)
