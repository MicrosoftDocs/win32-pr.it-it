---
title: Struttura float4x4 (Windowsnumerics.h)
description: Matrice 4x4, usata per le trasformazioni 3D.
ms.assetid: C0D2198A-B547-4153-AD02-9A47835FD272
keywords:
- Struttura float4x4
topic_type:
- apiref
api_name:
- float4x4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c918ee81ddac31d697ff3885e04e8cb530cd31a98f842c109f9d281786ee2539
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825271"
---
# <a name="float4x4-structure"></a>Struttura float4x4

Matrice 4x4, usata per le trasformazioni 3D.

Questo tipo di matrice usa un layout di vettore di riga. X, y e z del vettore di traslazione di questa matrice corrispondono ai campi m41, m42, m43.

Questo tipo è disponibile solo in C++. L'equivalente .NET è [System.Numerics.Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).

## <a name="constructors"></a>Costruttori

| Nome | Descrizione |
|-|-|
| `float4x4()` | Crea un float4x4 non inizializzato. |
| `float4x4(float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44)` | Crea un oggetto float4x4 con i valori specificati. |
| `explicit float4x4(float3x2 value)` | Crea un float4x4 da un float3x2. |
| `float4x4(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4 const& value)` | Converte **un oggetto Microsoft.Graphics.Canvas.Numerics.Matrix4x4** in float4x4. |

## <a name="functions"></a>Funzioni

| Nome | Descrizione |
|-|-|
| `float4x4 make_float4x4_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& cameraUpVector, float3 const& cameraForwardVector)` | Crea un manifesto sferico che ruota intorno a una posizione dell'oggetto specificata, usando un sistema di coordinate con la mano destra. |
| `float4x4 make_float4x4_?constrained_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& rotateAxis, float3 const& cameraForwardVector, float3 const& objectForwardVector)` | Crea un manifesto cilindrico che ruota intorno a un asse specificato, usando un sistema di coordinate con mano destra. |
| `float4x4 make_float4x4_translation(float3 const& position)` | Crea una matrice di traslazione. |
| `float4x4 make_float4x4_translation(float xPosition, float yPosition, float zPosition)` | Crea una matrice di traslazione. |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale)` | Crea una matrice di ridimensionamento, centrata sull'origine. |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale, float3 const& centerPoint)` | Crea una matrice di scala, centrata sul punto specificato. |
| `float4x4 make_float4x4_scale(float3 const& scales)` | Crea una matrice di ridimensionamento, centrata sull'origine. |
| `float4x4 make_float4x4_scale(float3 const& scales, float3 const& centerPoint)` | Crea una matrice di scala, centrata sul punto specificato. |
| `float4x4 make_float4x4_scale(float scale)` | Crea una matrice di ridimensionamento, centrata sull'origine. |
| `float4x4 make_float4x4_scale(float scale, float3 const& centerPoint)` | Crea una matrice di scala, centrata sul punto specificato. |
| `float4x4 make_float4x4_rotation_x(float radians)` | Crea una matrice di rotazione dell'asse X, centrata sull'origine. |
| `float4x4 make_float4x4_rotation_x(float radians, float3 const& centerPoint)` | Crea una matrice di rotazione dell'asse x, centrata sul punto specificato. |
| `float4x4 make_float4x4_rotation_y(float radians)` | Crea una matrice di rotazione dell'asse y, centrata sull'origine. |
| `float4x4 make_float4x4_rotation_y(float radians, float3 const& centerPoint)` | Crea una matrice di rotazione dell'asse y, centrata sul punto specificato. |
| `float4x4 make_float4x4_rotation_z(float radians)` | Crea una matrice di rotazione dell'asse z, centrata sull'origine. |
| `float4x4 make_float4x4_rotation_z(float radians, float3 const& centerPoint)` | Crea una matrice di rotazione dell'asse z, centrata sul punto specificato. |
| `float4x4 make_float4x4_from_axis_angle(float3 const& axis, float angle)` | Crea una matrice che ruota intorno a un vettore arbitrario. |
| `float4x4 make_float4x4_?perspective_field_of_view(float fieldOfView, float aspectRatio, float nearPlaneDistance, float farPlaneDistance)` | Crea una matrice di proiezione prospettica basata su un campo di visualizzazione, usando un sistema di coordinate con mano destra. |
| `float4x4 make_float4x4_perspective(float width, float height, float nearPlaneDistance, float farPlaneDistance)` | Crea una matrice di proiezione prospettica usando un sistema di coordinate con mano destra. |
| `float4x4 make_float4x4_?perspective_off_center(float left, float right, float bottom, float top, float nearPlaneDistance, float farPlaneDistance)` | Crea una matrice di proiezione prospettica personalizzata usando un sistema di coordinate con mano destra. |
| `float4x4 make_float4x4_orthographic(float width, float height, float zNearPlane, float zFarPlane)` | Crea una matrice di proiezione ortografica usando un sistema di coordinate con mano destra. |
| `float4x4 make_float4x4_?orthographic_off_center(float left, float right, float bottom, float top, float zNearPlane, float zFarPlane)` | Crea una matrice di proiezione ortografica personalizzata usando un sistema di coordinate con mano destra. |
| `float4x4 make_float4x4_look_at(float3 const& cameraPosition, float3 const& cameraTarget, float3 const& cameraUpVector)` | Crea una matrice di visualizzazione usando un sistema di coordinate con la mano destra. |
| `float4x4 make_float4x4_world(float3 const& position, float3 const& forward, float3 const& up)` | Crea una matrice globale usando un sistema di coordinate con mano destra. Può essere usato per posizionare gli oggetti nello spazio 3D. |
| `float4x4 make_float4x4_?from_quaternion(quaternion const& quaternion)` | Crea una matrice di rotazione da un quaternione. |
| `float4x4 make_float4x4_?from_yaw_pitch_roll(float yaw, float pitch, float roll)` | Crea una matrice di rotazione da un yaw, un passo e un rollio specificati. |
| `float4x4 make_float4x4_shadow(float3 const& lightDirection, plane const& plane)` | Crea una matrice che appiattisce la geometria in un piano specificato come se si proiettasse un'ombra da una sorgente di luce specificata. |
| `float4x4 make_float4x4_reflection(plane const& value)` | Crea una matrice che crea un sistema di coordinate speculare rispetto a un piano specificato. |
| `bool is_identity(float4x4 const& value)` | Verifica se si tratta di una matrice di identità. |
| `float determinant(float4x4 const& value)` | Calcola il determinante della matrice. |
| `float3 translation(float4x4 const& value)` | Ottiene il vettore di traslazione della matrice. |
| `bool invert(float4x4 const& matrix, _Out_ float4x4* result)` | Calcola l'inverso di una matrice. Restituisce true se la matrice può essere invertita; false in caso contrario. |
| `bool decompose(float4x4 const& matrix, _Out_ float3* scale, _Out_ quaternion* rotation, _Out_ float3* translation)` | Estrae i componenti scalari, di traslazione e di rotazione da una matrice SRT (Scale/Rotate/Translate) 3D. Restituisce true se la matrice può essere scomposta; false in caso contrario. |
| `float4x4 transform(float4x4 const& value, quaternion const& rotation)` | Trasforma una matrice applicando una rotazione quaternione. |
| `float4x4 transpose(float4x4 const& matrix)` | Trasponi i componenti di una matrice lungo la diagonale. |
| `float4x4 lerp(float4x4 const& matrix1, float4x4 const& matrix2, float amount)` | Interpolazione lineare tra i valori corrispondenti di due matrici. |

## <a name="methods"></a>Metodi

| Nome | Descrizione |
|-|-|
| `static float4x4 identity()` | Restituisce un'istanza della matrice di identità. |

## <a name="operators"></a>Operatori

| Nome | Descrizione |
|-|-|
| `float4x4 operator+ (float4x4 const& value1, float4x4 const& value2)` | Aggiunge ogni componente di una matrice a un'altra matrice. |
| `float4x4 operator- (float4x4 const& value1, float4x4 const& value2)` | Sottrae ogni componente di una matrice da un'altra matrice. |
| `float4x4 operator* (float4x4 const& value1, float4x4 const& value2)` | Moltiplica una matrice per un'altra matrice. Ciò ha l'effetto di concatenare due trasformazioni. |
| `float4x4 operator* (float4x4 const& value1, float value2)` | Moltiplica ogni componente di una matrice per un valore scalare. |
| `float4x4 operator- (float4x4 const& value)` | Nega ogni componente di una matrice. |
| `float4x4& operator+= (float4x4& value1, float4x4 const& value2)` | Sul posto aggiunge ogni componente di una matrice a un'altra matrice. |
| `float4x4& operator-= (float4x4& value1, float4x4 const& value2)` | Sul posto sottrae ogni componente di una matrice da un'altra matrice. |
| `float4x4& operator*= (float4x4& value1, float4x4 const& value2)` | Sul posto moltiplica una matrice per un'altra matrice. Ciò ha l'effetto di concatenare due trasformazioni. |
| `float4x4& operator*= (float4x4& value1, float value2)` | Sul posto moltiplica ogni componente di una matrice per un valore scalare. |
| `bool operator== (float4x4 const& value1, float4x4 const& value2)` | Determina se due istanze di float4x4 sono uguali. |
| `bool operator!= (float4x4 const& value1, float4x4 const& value2)` | Determina se due istanze di float4x4 non sono uguali. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4() const` | Converte un float4x4 in **microsoft.Graphics.Canvas.Numerics.Matrix4x4.** |

## <a name="fields"></a>Campi

| Nome | Descrizione |
|-|-|
| `float m11` | Valore alla riga 1 colonna 1 della matrice. |
| `float m12` | Valore alla riga 1 colonna 2 della matrice. |
| `float m13` | Valore alla riga 1 colonna 3 della matrice. |
| `float m14` | Valore alla riga 1 colonna 4 della matrice. |
| `float m21` | Valore alla riga 2 colonna 1 della matrice. |
| `float m22` | Valore alla riga 2 colonna 2 della matrice. |
| `float m23` | Valore alla riga 2 colonna 3 della matrice. |
| `float m24` | Valore alla riga 2 colonna 4 della matrice. |
| `float m31` | Valore alla riga 3 colonna 1 della matrice. |
| `float m32` | Valore alla riga 3 colonna 2 della matrice. |
| `float m33` | Valore alla riga 3 colonna 3 della matrice. |
| `float m34` | Valore alla riga 3 colonna 4 della matrice. |
| `float m41` | Valore alla riga 4 colonna 1 della matrice. |
| `float m42` | Valore alla riga 4 colonna 2 della matrice. |
| `float m43` | Valore alla riga 4 colonna 3 della matrice. |
| `float m44` | Valore alla riga 4 colonna 4 della matrice. |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Spazio dei nomi | Windows::Foundation::Numerics |
| Intestazione | <dl> <dt>Windowsnumerics.h</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[API windowsnumerics.h](windowsnumerics-h-apis-portal.md)
