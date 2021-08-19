---
title: Struttura float3 (Windowsnumerics.h)
description: Vettore con tre componenti.
ms.assetid: CAA10ADA-C5A8-4B75-A0A9-5C5B3FDD9A07
keywords:
- Struttura float3
topic_type:
- apiref
api_name:
- float3 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521c63f99c35e68f18d9a6c0a81118f647ff131effb0f6528e2ef3882c43e234
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939514"
---
# <a name="float3-structure"></a>Struttura float3

Vettore con tre componenti.

Questo tipo è disponibile solo in C++. L'equivalente .NET è [System.Numerics.Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).

## <a name="constructors"></a>Costruttori

| Nome | Descrizione |
|-|-|
| `float3()` | Crea un float3 non inizializzato. |
| `float3(float x, float y, float z)` | Crea un oggetto float3 con i valori specificati. |
| `float3(float2 value, float z)` | Crea un oggetto float3 con x e y copiati da float2 più il valore z specificato. |
| `explicit float3(float value)` | Crea un oggetto float3 con tutti i componenti impostati sul valore specificato. |
| `float3(Microsoft::Graphics::Canvas::Numerics::Vector3 const& value)` | Converte **un oggetto Microsoft.Graphics.Canvas.Numerics.Vector3** in float3. |

## <a name="functions"></a>Funzioni

| Nome | Descrizione |
|-|-|
| `float length(float3 const& value)` | Calcola la lunghezza, o distanza euclidea, del vettore. |
| `float length_squared(float3 const& value)` | Calcola la lunghezza, o distanza euclidea, del vettore al quadrato. |
| `float distance(float3 const& value1, float3 const& value2)` | Calcola la distanza euclidea tra due vettori. |
| `float distance_squared(float3 const& value1, float3 const& value2)` | Calcola la distanza euclidea tra due vettori al quadrato. |
| `float dot(float3 const& vector1, float3 const& vector2)` | Calcola il prodotto del punto di due vettori. |
| `float3 normalize(float3 const& value)` | Crea un vettore di unità dal vettore specificato. |
| `float3 cross(float3 const& vector1, float3 const& vector2)` | Calcola il prodotto incrociato di due vettori. |
| `float3 reflect(float3 const& vector, float3 const& normal)` | Determina il vettore di riflessione del vettore e della normale specificati. |
| `float3 min(float3 const& value1, float3 const& value2)` | Restituisce un vettore che contiene il valore più basso di ogni coppia di componenti corrispondente. |
| `float3 max(float3 const& value1, float3 const& value2)` | Restituisce un vettore che contiene il valore più alto di ogni coppia di componenti corrispondente. |
| `float3 clamp(float3 const& value1, float3 const& min, float3 const& max)` | Limita un valore in modo che sia compreso in un intervallo specificato. |
| `float3 lerp(float3 const& value1, float3 const& value2, float amount)` | Esegue un'interpolazione lineare tra due vettori. |
| `float3 transform(float3 const& position, float4x4 const& matrix)` | Trasforma il vettore (x, y, z, 1) in base alla matrice specificata. |
| `float3 transform_normal(float3 const& normal, float4x4 const& matrix)` | Trasforma il vettore normale (x, y, z, 0) in base alla matrice specificata. |
| `float3 transform(float3 const& value, quaternion const& rotation)` | Trasforma un float3 in base al quaternione specificato. |

## <a name="methods"></a>Metodi

| Nome | Descrizione |
|-|-|
| `static float3 zero()` | Restituisce un valore float3 con tutti i relativi componenti impostati su zero. |
| `static float3 one()` | Restituisce un valore float3 con tutti i relativi componenti impostati su uno. |
| `static float3 unit_x()` | Restituisce float3 (1, 0, 0). |
| `static float3 unit_y()` | Restituisce float3 (0, 1, 0). |
| `static float3 unit_z()` | Restituisce float3 (0, 0, 1). |

## <a name="operators"></a>Operatori

| Nome | Descrizione |
|-|-|
| `float3 operator+ (float3 const& value1, float3 const& value2)` | Aggiunge due vettori. |
| `float3 operator- (float3 const& value1, float3 const& value2)` | Sottrae un vettore da un vettore. |
| `float3 operator* (float3 const& value1, float3 const& value2)` | Moltiplica i componenti di due vettori l'uno per l'altro. |
| `float3 operator* (float3 const& value1, float value2)` | Moltiplica un vettore per uno scalare. |
| `float3 operator* (float value1, float3 const& value2)` | Moltiplica un vettore per uno scalare. |
| `float3 operator/ (float3 const& value1, float3 const& value2)` | Divide i componenti di un vettore per i componenti di un altro vettore. |
| `float3 operator/ (float3 const& value1, float value2)` | Divide un vettore per un valore scalare. |
| `float3 operator- (float3 const& value)` | Restituisce un vettore che punta nella direzione opposta. |
| `float3& operator+= (float3& value1, float3 const& value2)` | Sul posto aggiunge due vettori. |
| `float3& operator-= (float3& value1, float3 const& value2)` | Sul posto sottrae un vettore da un vettore. |
| `float3& operator*= (float3& value1, float3 const& value2)` | Sul posto moltiplica i componenti di due vettori l'uno per l'altro. |
| `float3& operator*= (float3& value1, float value2)` | Sul posto moltiplica un vettore per uno scalare. |
| `float3& operator/= (float3& value1, float3 const& value2)` | Sul posto divide i componenti di un vettore per i componenti di un altro vettore. |
| `float3& operator/= (float3& value1, float value2)` | Sul posto divide un vettore per un valore scalare. |
| `bool operator== (float3 const& value1, float3 const& value2)` | Determina se due istanze di float3 sono uguali. |
| `bool operator!= (float3 const& value1, float3 const& value2)` | Determina se due istanze di float3 non sono uguali. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector3() const` | Converte un oggetto float3 in **un oggetto Microsoft.Graphics.Canvas.Numerics.Vector3.** |

## <a name="fields"></a>Campi

| Nome | Descrizione |
|-|-|
| `float x` | Componente X del vettore. |
| `float y` | Componente Y del vettore. |
| `float z` | Componente Z del vettore. |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Spazio dei nomi | Windows::Foundation::Numerics |
| Intestazione | <dl> <dt>Windowsnumerics.h</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[API windowsnumerics.h](windowsnumerics-h-apis-portal.md)
