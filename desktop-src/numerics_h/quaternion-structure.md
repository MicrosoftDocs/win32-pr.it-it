---
title: struttura Quaternion (Windowsnumerics. h)
description: Vettore a quattro dimensioni, usato per rappresentare una rotazione.
ms.assetid: A6B25885-8ECB-4039-9DC6-41D5F3A02489
keywords:
- struttura Quaternion
topic_type:
- apiref
api_name:
- quaternion structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ae169232f83e6753505f9d5d07fffac09e67e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332789"
---
# <a name="quaternion-structure"></a>Struttura Quaternion

Vettore a quattro dimensioni, usato per rappresentare una rotazione.

Un quaternione può ruotare in modo efficiente un oggetto relativo al vettore (x, y, z) in base all'angolo theta, dove w = cos (theta/2). I quaternioni vengono in genere usati per l'interpolazione uniforme tra due angoli e per evitare il problema di blocco del cardano che può verificarsi con gli angoli di Eulero.

Questo tipo è disponibile solo in C++. Il relativo equivalente .NET è [System. Numerics. Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).

## <a name="constructors"></a>Costruttori

| Nome | Descrizione |
|-|-|
| `quaternion()` | Crea un quaternione non inizializzato. |
| `quaternion(float x, float y, float z, float w)` | Crea un quaternione con i valori specificati. |
| `quaternion(float3 vectorPart, float scalarPart)` | Crea un quaternione da un float3 e scalare. |
| `quaternion(Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion const& value)` | Converte un oggetto **Microsoft. graphics. Canvas. Numerics. Quaternion** in un quaternione. |

## <a name="functions"></a>Funzioni

| Nome | Descrizione |
|-|-|
| `quaternion make_quaternion_from_axis_angle(float3 const& axis, float angle)` | Crea un quaternione da un vettore e un angolo per la rotazione intorno al vettore. |
| `quaternion make_quaternion_from_yaw_pitch_roll(float yaw, float pitch, float roll)` | Crea un quaternione dagli angoli specificati per l'imbardata, il pitch e il roll. |
| `quaternion make_quaternion_from_rotation_matrix(float4x4 const& matrix)` | Crea un quaternione da una matrice di rotazione. |
| `bool is_identity(quaternion const& value)` | Verifica se si tratta di un quaternione Identity (nessuna rotazione). |
| `float length(quaternion const& value)` | Calcola la lunghezza di un quaternione. |
| `float length_squared(quaternion const& value)` | Calcola la lunghezza quadrata di un quaternione. |
| `float dot(quaternion const& quaternion1, quaternion const& quaternion2)` | Calcola il prodotto scalare di due quaternioni. |
| `quaternion normalize(quaternion const& value)` | Divide ogni componente di un quaternione per la lunghezza del quaternione. |
| `quaternion conjugate(quaternion const& value)` | Calcola il coniugato di un quaternione. |
| `quaternion inverse(quaternion const& value)` | Calcola l'inverso di un quaternione. |
| `quaternion slerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | Esegue l'interpolazione tra due quaternioni usando l'interpolazione lineare sferica. |
| `quaternion lerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | Interpolazione lineare tra due quaternioni. |
| `quaternion concatenate(quaternion const& value1, quaternion const& value2)` | Concatena due quaternioni; il risultato rappresenta la prima rotazione seguita dalla seconda rotazione. |

## <a name="methods"></a>Metodi

| Nome | Descrizione |
|-|-|
| `static quaternion identity()` | Restituisce un'istanza del quaternione di identità. |

## <a name="operators"></a>Operatori

| Nome | Descrizione |
|-|-|
| `quaternion operator+ (quaternion const& value1, quaternion const& value2)` | Aggiunge due quaternioni. |
| `quaternion operator- (quaternion const& value1, quaternion const& value2)` | Sottrae un quaternione da un altro quaternione. |
| `quaternion operator* (quaternion const& value1, quaternion const& value2)` | Moltiplica un quaternione per un altro quaternione. |
| `quaternion operator* (quaternion const& value1, float value2)` | Moltiplica un quaternione per un valore scalare. |
| `quaternion operator/ (quaternion const& value1, quaternion const& value2)` | Divide un quaternione da un altro quaternione. |
| `quaternion operator- (quaternion const& value)` | Capovolge il segno di ogni componente del quaternione. |
| `quaternion& operator+= (quaternion& value1, quaternion const& value2)` | Sul posto vengono aggiunti due quaternioni. |
| `quaternion& operator-= (quaternion& value1, quaternion const& value2)` | Il sul posto sottrae un quaternione da un altro quaternione. |
| `quaternion& operator*= (quaternion& value1, quaternion const& value2)` | Sul posto moltiplica un quaternione per un altro quaternione. |
| `quaternion& operator*= (quaternion& value1, float value2)` | Nultiplies sul posto di un quaternione da un valore scalare. |
| `quaternion& operator/= (quaternion& value1, quaternion const& value2)` | Sul posto divide un quaternione da un altro quaternione. |
| `bool operator== (quaternion const& value1, quaternion const& value2)` | Determina se due istanze del quaternione sono uguali. |
| `bool operator!= (quaternion const& value1, quaternion const& value2)` | Determina se due istanze di Quaternion non sono uguali. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion() const` | Converte un quaternione in un oggetto **Microsoft. graphics. Canvas. Numerics. Quaternion**. |

## <a name="fields"></a>Campi

| Nome | Descrizione |
|-|-|
| `float x` | Valore X del componente Vector del quaternione. |
| `float y` | Valore Y del componente Vector del quaternione. |
| `float z` | Valore Z del componente Vector del quaternione. |
| `float w` | Componente di rotazione del quaternione. |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Spazio dei nomi | Windows:: Foundation:: Numerics |
| Intestazione | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[API windowsnumerics. h](windowsnumerics-h-apis-portal.md)
