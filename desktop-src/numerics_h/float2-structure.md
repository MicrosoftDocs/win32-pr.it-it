---
title: struttura float2 (Windowsnumerics. h)
description: Vettore con due componenti.
ms.assetid: 1A23C1E3-F34F-4249-80EA-92A13CD4B34F
keywords:
- struttura float2
topic_type:
- apiref
api_name:
- float2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72398bdc087e0f7a0845703a2cefea40b5465b21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332805"
---
# <a name="float2-structure"></a>struttura float2

Vettore con due componenti.

Questo tipo è disponibile solo in C++. L'equivalente .NET è [System. Numerics. Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).

## <a name="constructors"></a>Costruttori

| Nome | Descrizione |
|-|-|
| `float2()` | Crea un float2 non inizializzato. |
| `float2(float x, float y)` | Crea un float2 con i valori specificati. |
| `explicit float2(float value)` | Crea un float2 con tutti i componenti impostati sul valore specificato. |
| `float2(Microsoft::Graphics::Canvas::Numerics::Vector2 const& value)` | Converte un oggetto **Microsoft. graphics. Canvas. Numerics. Vector2** in un float2. |
| `float2(Windows::Foundation::Point const& value)` | Converte un oggetto [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point) in un float2. |
| `float2(Windows::Foundation::Size const& value)` | Converte un oggetto [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size) in un float2. |

## <a name="functions"></a>Funzioni

| Nome | Descrizione |
|-|-|
| `float length(float2 const& value)` | Calcola la lunghezza o la distanza euclidea del vettore. |
| `float length_squared(float2 const& value)` | Calcola la lunghezza o la distanza euclidea del vettore quadrato. |
| `float distance(float2 const& value1, float2 const& value2)` | Calcola la distanza euclidea tra due vettori. |
| `float distance_squared(float2 const& value1, float2 const& value2)` | Calcola la distanza euclidea tra due vettori quadrati. |
| `float dot(float2 const& value1, float2 const& value2)` | Calcola il prodotto a punti di due vettori. |
| `float2 normalize(float2 const& value)` | Crea un vettore di unità dal vettore specificato. |
| `float2 reflect(float2 const& vector, float2 const& normal)` | Determina il vettore di reflection del vettore specificato e il normale. |
| `float2 min(float2 const& value1, float2 const& value2)` | Restituisce un vettore che contiene il valore più basso di ogni coppia di componenti corrispondente. |
| `float2 max(float2 const& value1, float2 const& value2)` | Restituisce un vettore che contiene il valore massimo di ogni coppia di componenti corrispondente. |
| `float2 clamp(float2 const& value1, float2 const& min, float2 const& max)` | Limita un valore all'interno di un intervallo specificato. |
| `float2 lerp(float2 const& value1, float2 const& value2, float amount)` | Esegue un'interpolazione lineare tra due vettori. |
| `float2 transform(float2 const& position, float3x2 const& matrix)` | Trasforma il vettore (x, y, 0, 1) in base alla matrice specificata. |
| `float2 transform(float2 const& position, float4x4 const& matrix)` | Trasforma il vettore (x, y, 0, 1) in base alla matrice specificata. |
| `float2 transform_normal(float2 const& normal, float3x2 const& matrix)` | Trasforma il vettore normale (x, y, 0, 0) in base alla matrice specificata. |
| `float2 transform_normal(float2 const& normal, float4x4 const& matrix)` | Trasforma il vettore normale (x, y, 0, 0) in base alla matrice specificata. |
| `float2 transform(float2 const& value, quaternion const& rotation)` | Trasforma un float2 in base al quaternione specificato. |

## <a name="methods"></a>Metodi

| Nome | Descrizione |
|-|-|
| `static float2 zero()` | Restituisce un float2 con tutti i relativi componenti impostati su zero. |
| `static float2 one()` | Restituisce un float2 con tutti i relativi componenti impostati su uno. |
| `static float2 unit_x()` | Restituisce float2 (1,0). |
| `static float2 unit_y()` | Restituisce float2 (0, 1). |

## <a name="operators"></a>Operatori

| Nome | Descrizione |
|-|-|
| `operator Windows::Foundation::Point() const` | Converte un float2 in un oggetto [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point). |
| `operator Windows::Foundation::Size() const` | Converte un float2 in un oggetto [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size). |
| `float2 operator+ (float2 const& value1, float2 const& value2)` | Aggiunge due vettori. |
| `float2 operator- (float2 const& value1, float2 const& value2)` | Sottrae un vettore da un vettore. |
| `float2 operator* (float2 const& value1, float2 const& value2)` | Moltiplica i componenti di due vettori. |
| `float2 operator* (float2 const& value1, float value2)` | Moltiplica un vettore per un valore scalare. |
| `float2 operator* (float value1, float2 const& value2)` | Moltiplica un vettore per un valore scalare. |
| `float2 operator/ (float2 const& value1, float2 const& value2)` | Divide i componenti di un vettore in base ai componenti di un altro vettore. |
| `float2 operator/ (float2 const& value1, float value2)` | Divide un vettore per un valore scalare. |
| `float2 operator- (float2 const& value)` | Restituisce un vettore che punta nella direzione opposta. |
| `float2& operator+= (float2& value1, float2 const& value2)` | Sul posto vengono aggiunti due vettori. |
| `float2& operator-= (float2& value1, float2 const& value2)` | Il sul posto sottrae un vettore da un vettore. |
| `float2& operator*= (float2& value1, float2 const& value2)` | Sul posto moltiplica i componenti di due vettori. |
| `float2& operator*= (float2& value1, float value2)` | Sul posto moltiplica un vettore per un valore scalare. |
| `float2& operator/= (float2& value1, float2 const& value2)` | Sul posto divide i componenti di un vettore in base ai componenti di un altro vettore. |
| `float2& operator/= (float2& value1, float value2)` | Sul posto divide un vettore per un valore scalare. |
| `bool operator== (float2 const& value1, float2 const& value2)` | Determina se due istanze di float2 sono uguali. |
| `bool operator!= (float2 const& value1, float2 const& value2)` | Determina se due istanze di float2 non sono uguali. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector2() const` | Converte un float2 in un oggetto **Microsoft. graphics. Canvas. Numerics. Vector2**. |

## <a name="fields"></a>Campi

| Nome | Descrizione |
|-|-|
| `float x` | Componente X del vettore. |
| `float y` | Componente Y del vettore. |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Spazio dei nomi | Windows:: Foundation:: Numerics |
| Intestazione | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[API windowsnumerics. h](windowsnumerics-h-apis-portal.md)
