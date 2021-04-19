---
title: struttura float3x2 (Windowsnumerics. h)
description: Matrice 3x2 utilizzata per le trasformazioni 2D.
ms.assetid: 5C2A4C30-3EC4-4DE9-A42A-6A19F96F8D69
keywords:
- struttura float3x2
topic_type:
- apiref
api_name:
- float3x2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9351fae9636ca2512825c7df5383eddf1558583e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332803"
---
# <a name="float3x2-structure"></a>struttura float3x2

Matrice 3x2 utilizzata per le trasformazioni 2D.

Questo tipo di matrice utilizza un layout vettoriale di riga. Le x e y del vettore di traduzione della matrice corrispondono ai campi M31, M32.

Questo tipo è disponibile solo in C++. Il relativo equivalente .NET è [System. Numerics. Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).

## <a name="constructors"></a>Costruttori

| Nome | Descrizione |
|-|-|
| `float3x2()` | Crea un float3x2 non inizializzato. |
| `float3x2(float m11, float m12, float m21, float m22, float m31, float m32)` | Crea un float3x2 con i valori specificati. |
| `float3x2(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2 const& value)` | Converte un oggetto **Microsoft. graphics. Canvas. Numerics. Matrix3x2** in un float3x2. |

## <a name="functions"></a>Funzioni

| Nome | Descrizione |
|-|-|
| `float3x2 make_float3x2_translation(float2 const& position)` | Crea una matrice di traslazione. |
| `float3x2 make_float3x2_translation(float xPosition, float yPosition)` | Crea una matrice di traslazione. |
| `float3x2 make_float3x2_scale(float xScale, float yScale)` | Crea una matrice di scala, centrata sull'origine. |
| `float3x2 make_float3x2_scale(float xScale, float yScale, float2 const& centerPoint)` | Crea una matrice di scala, centrata sul punto specificato. |
| `float3x2 make_float3x2_scale(float2 const& scales)` | Crea una matrice di scala, centrata sull'origine. |
| `float3x2 make_float3x2_scale(float2 const& scales, float2 const& centerPoint)` | Crea una matrice di scala, centrata sul punto specificato. |
| `float3x2 make_float3x2_scale(float scale)` | Crea una matrice di scala, centrata sull'origine. |
| `float3x2 make_float3x2_scale(float scale, float2 const& centerPoint)` | Crea una matrice di scala, centrata sul punto specificato. |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY)` | Crea una matrice di inclinazione, centrata sull'origine. |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY, float2 const& centerPoint)` | Crea una matrice di inclinazione, centrata sul punto specificato. |
| `float3x2 make_float3x2_rotation(float radians)` | Crea una matrice di rotazione, centrata sull'origine. |
| `float3x2 make_float3x2_rotation(float radians, float2 const& centerPoint)` | Crea una matrice di rotazione, centrata sul punto specificato. |
| `bool is_identity(float3x2 const& value)` | Verifica se si tratta di una matrice di identità. |
| `float determinant(float3x2 const& value)` | Calcola il determinante della matrice. |
| `float2 translation(float3x2 const& value)` | Ottiene il vettore di traslazione della matrice. |
| `bool invert(float3x2 const& matrix, _Out_ float3x2* result)` | Calcola l'inverso di una matrice. Restituisce true se la matrice può essere invertita; in caso contrario, false. |
| `float3x2 lerp(float3x2 const& matrix1, float3x2 const& matrix2, float amount)` | Esegue l'interpolazione lineare tra i valori corrispondenti di due matrici. |

## <a name="methods"></a>Metodi

| Nome | Descrizione |
|-|-|
| `static float3x2 identity()` | Restituisce un'istanza della matrice di identità. |

## <a name="operators"></a>Operatori

| Nome | Descrizione |
|-|-|
| `float3x2 operator+ (float3x2 const& value1, float3x2 const& value2)` | Aggiunge ogni componente di una matrice a un'altra matrice. |
| `float3x2 operator- (float3x2 const& value1, float3x2 const& value2)` | Sottrae ogni componente di una matrice da un'altra matrice. |
| `float3x2 operator* (float3x2 const& value1, float3x2 const& value2)` | Moltiplica una matrice per un'altra matrice. Questo ha l'effetto di concatenare due trasformazioni. |
| `float3x2 operator* (float3x2 const& value1, float value2)` | Moltiplica ogni componente di una matrice in base a un valore scalare. |
| `float3x2 operator- (float3x2 const& value)` | Nega ogni componente di una matrice. |
| `float3x2& operator+= (float3x2& value1, float3x2 const& value2)` | Sul posto aggiunge ogni componente di una matrice a un'altra matrice. |
| `float3x2& operator-= (float3x2& value1, float3x2 const& value2)` | Il sul posto sottrae ogni componente di una matrice da un'altra matrice. |
| `float3x2& operator*= (float3x2& value1, float3x2 const& value2)` | Sul posto viene moltiplicata una matrice da un'altra matrice. Questo ha l'effetto di concatenare due trasformazioni. |
| `float3x2& operator*= (float3x2& value1, float value2)` | Sul posto moltiplica ogni componente di una matrice per un valore scalare. |
| `bool operator== (float3x2 const& value1, float3x2 const& value2)` | Determina se due istanze di float3x2 sono uguali. |
| `bool operator!= (float3x2 const& value1, float3x2 const& value2)` | Determina se due istanze di float3x2 non sono uguali. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2() const` | Converte un float3x2 in un oggetto **Microsoft. graphics. Canvas. Numerics. Matrix3x2**. |

## <a name="fields"></a>Campi

| Nome | Descrizione |
|-|-|
| `float m11` | Valore alla riga 1 colonna 1 della matrice. |
| `float m12` | Valore alla riga 1 colonna 2 della matrice. |
| `float m21` | Valore alla riga 2 colonna 1 della matrice. |
| `float m22` | Valore alla riga 2 colonna 2 della matrice. |
| `float m31` | Valore alla riga 3 della colonna 1 della matrice. |
| `float m32` | Valore alla riga 3 colonna 2 della matrice. |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Spazio dei nomi | Windows:: Foundation:: Numerics |
| Intestazione | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[API windowsnumerics. h](windowsnumerics-h-apis-portal.md)
