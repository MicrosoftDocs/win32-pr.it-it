---
title: Struttura float4 (Windowsnumerics.h)
description: Vettore con quattro componenti.
ms.assetid: AC07C6D0-E7FD-4582-B40D-4838F49FB8B4
keywords:
- Struttura float4
topic_type:
- apiref
api_name:
- float4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb1af9bee9a571abf58fb20539945effc3ff1ee81cbb48a4d90c1510aebcd4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825281"
---
# <a name="float4-structure"></a>Struttura float4

Vettore con quattro componenti.

Questo tipo è disponibile solo in C++. L'equivalente di .NET è [System.Numerics.Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).

## <a name="constructors"></a>Costruttori

| Nome | Descrizione |
|-|-|
| `float4()` | Crea un float4 non inizializzato. |
| `float4(float x, float y, float z, float w)` | Crea un oggetto float4 con i valori specificati. |
| `float4(float2 value, float z, float w)` | Crea un oggetto float4 con x e y copiati da float2 più i valori z e w specificati. |
| `float4(float3 value, float w)` | Crea un oggetto float4 con x, y e z copiati da float3 più il valore w specificato. |
| `explicit float4(float value)` | Crea un float4 con tutti i com.ents impostati sul valore specificato. |
| `float4(Microsoft::?Graphics::?Canvas::?Numerics::?Vector4 const& value)` | Converte **un oggetto Microsoft.Graphics.Canvas.Numerics.Vector4** in float4. |

## <a name="functions"></a>Funzioni

| Nome | Descrizione |
|-|-|
| `float length(float4 const& value)` | Calcola la lunghezza, o distanza euclidea, del vettore. |
| `float length_squared(float4 const& value)` | Calcola la lunghezza, o distanza euclidea, del vettore al quadrato. |
| `float distance(float4 const& value1, float4 const& value2)` | Calcola la distanza euclidea tra due vettori. |
| `float distance_squared(float4 const& value1, float4 const& value2)` | Calcola la distanza euclidea tra due vettori al quadrato. |
| `float dot(float4 const& vector1, float4 const& vector2)` | Calcola il prodotto del punto di due vettori. |
| `float4 normalize(float4 const& vector)` | Crea un vettore di unità dal vettore specificato. |
| `float4 min(float4 const& value1, float4 const& value2)` | Restituisce un vettore che contiene il valore più basso di ogni coppia di componenti corrispondente. |
| `float4 max(float4 const& value1, float4 const& value2)` | Restituisce un vettore che contiene il valore più alto di ogni coppia di componenti corrispondente. |
| `float4 clamp(float4 const& value1, float4 const& min, float4 const& max)` | Limita un valore in modo che sia compreso in un intervallo specificato. |
| `float4 lerp(float4 const& value1, float4 const& value2, float amount)` | Esegue un'interpolazione lineare tra due vettori. |
| `float4 transform(float4 const& vector, float4x4 const& matrix)` | Trasforma un float4 in base alla matrice specificata. |
| `float4 transform4(float3 const& position, float4x4 const& matrix)` | Trasforma un float3 in base alla matrice specificata, restituisce un oggetto float4. |
| `float4 transform4(float2 const& position, float4x4 const& matrix)` | Trasforma un oggetto float2 in base alla matrice specificata, restituisce un oggetto float4. |
| `float4 transform(float4 const& value, quaternion const& rotation)` | Trasforma un float4 in base al quaternione specificato. |
| `float4 transform4(float3 const& value, quaternion const& rotation)` | Trasforma un float3 dal quaternione specificato, restituisce un float4. |
| `float4 transform4(float2 const& value, quaternion const& rotation)` | Trasforma un oggetto float2 in base al quaternione specificato, restituisce un float4. |

## <a name="methods"></a>Metodi

| Nome | Descrizione |
|-|-|
| `static float4 zero()` | Restituisce un valore float4 con tutti i relativi componenti impostati su zero. |
| `static float4 one()` | Restituisce un valore float4 con tutti i relativi componenti impostati su uno. |
| `static float4 unit_x()` | Restituisce float4 (1, 0, 0, 0). |
| `static float4 unit_y()` | Restituisce float4 (0, 1, 0, 0). |
| `static float4 unit_z()` | Restituisce float4 (0, 0, 1, 0). |
| `static float4 unit_w()` | Restituisce float4 (0, 0, 0, 1). |

## <a name="operators"></a>Operatori

| Nome | Descrizione |
|-|-|
| `float4 operator+ (float4 const& value1, float4 const& value2)` | Aggiunge due vettori. |
| `float4 operator- (float4 const& value1, float4 const& value2)` | Sottrae un vettore da un vettore. |
| `float4 operator* (float4 const& value1, float4 const& value2)` | Moltiplica i componenti di due vettori l'uno per l'altro. |
| `float4 operator* (float4 const& value1, float value2)` | Moltiplica un vettore per uno scalare. |
| `float4 operator* (float value1, float4 const& value2)` | Moltiplica un vettore per uno scalare. |
| `float4 operator/ (float4 const& value1, float4 const& value2)` | Divide i componenti di un vettore per i componenti di un altro vettore. |
| `float4 operator/ (float4 const& value1, float value2)` | Divide un vettore per un valore scalare. |
| `float4 operator- (float4 const& value)` | Restituisce un vettore che punta nella direzione opposta. |
| `float4& operator+= (float4& value1, float4 const& value2)` | Sul posto aggiunge due vettori. |
| `float4& operator-= (float4& value1, float4 const& value2)` | Sul posto sottrae un vettore da un vettore. |
| `float4& operator*= (float4& value1, float4 const& value2)` | Sul posto moltiplica i componenti di due vettori l'uno per l'altro. |
| `float4& operator*= (float4& value1, float value2)` | Sul posto moltiplica un vettore per uno scalare. |
| `float4& operator/= (float4& value1, float4 const& value2)` | Sul posto divide i componenti di un vettore per i componenti di un altro vettore. |
| `float4& operator/= (float4& value1, float value2)` | Sul posto divide un vettore per un valore scalare. |
| `bool operator== (float4 const& value1, float4 const& value2)` | Determina se due istanze di float4 sono uguali. |
| `bool operator!= (float4 const& value1, float4 const& value2)` | Determina se due istanze di float4 non sono uguali. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector4() const` | Converte un oggetto float4 in **un oggetto Microsoft.Graphics.Canvas.Numerics.Vector4**. |

## <a name="fields"></a>Campi

| Nome | Descrizione |
|-|-|
| `float x` | Componente X del vettore. |
| `float y` | Componente Y del vettore. |
| `float z` | Componente Z del vettore. |
| `float w` | Componente W del vettore. |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Spazio dei nomi | Windows::Foundation::Numerics |
| Intestazione | <dl> <dt>Windowsnumerics.h</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[API windowsnumerics.h](windowsnumerics-h-apis-portal.md)
