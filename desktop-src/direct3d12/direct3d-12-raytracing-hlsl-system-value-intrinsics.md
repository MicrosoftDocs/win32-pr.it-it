---
title: Oggetti intrinseci dei valori di sistema HLSL raytracing di Direct3D 12
description: Visualizzare i collegamenti ad articoli che descrivono funzioni intrinseche intrinseche del valore di sistema HLSL (High-Level Shader Language) che supportano la pipeline di raytracing Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b2a2cbd870da41df94ee0389757a1d1ec7cd5e4549a3abd32dbaaf6a7c8e8e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045559"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a>Oggetti intrinseci dei valori di sistema HLSL raytracing di Direct3D 12

I valori di sistema vengono recuperati usando funzioni intrinseche speciali, anziché includere parametri con semantica speciale nella firma della funzione shader. 

## <a name="in-this-section"></a>Contenuto della sezione

### <a name="ray-dispatch-system-values"></a>Valori del sistema ray dispatch

| Argomento | Descrizione |
|-|-|
| [**DispatchRaysIndex**](dispatchraysindex.md) | Ottiene la posizione x e y corrente all'interno della larghezza e dell'altezza ottenute con il valore di sistema **DispatchRaysDimensions** intrinseco. |
| [**DispatchRaysDimensions**](dispatchraysdimensions.md) | Valori di larghezza, altezza e profondità della struttura **D3D12 \_ DISPATCH \_ RAYS \_ DESC** specificata nella chiamata **DispatchRays di** origine. |

### <a name="ray-system-values"></a>Valori del sistema di raggi

| Argomento | Descrizione |
|-|-|
| [**WorldRayOrigin**](worldrayorigin.md) | Origine dello spazio del mondo del raggio corrente. |
| [**WorldRayDirection**](worldraydirection.md) | Direzione dello spazio del mondo per il raggio corrente. |
| [**RayTMin**](raytmin.md) | Valore float che rappresenta il punto iniziale parametrico corrente per il raggio. |
| [**RayTCurrent**](raytcurrent.md) | Valore float che rappresenta il punto finale parametrico corrente per il raggio.  |
| [**RayFlags**](rayflags.md) | Intero senza segno contenente i **flag** ray_flag corrente. |

### <a name="primitiveobject-space-system-values"></a>Valori di sistema dello spazio degli oggetti/primitivi

| Argomento | Descrizione |
|-|-|
| [**InstanceIndex**](instanceindex.md) | Indice rigenerato automaticamente dell'istanza corrente nella struttura di accelerazione raytracing di primo livello. |
| [**Instanceid**](instanceid.md) | Identificatore fornito dall'utente per l'istanza nell'istanza della struttura di accelerazione di livello inferiore all'interno della struttura di primo livello. |
| [**PrimitiveIndex**](primitiveindex.md) | Indice rigenerato automaticamente della primitiva all'interno della geometria all'interno dell'istanza della struttura di accelerazione di livello inferiore. |
| [**ObjectRayOrigin**](objectrayorigin.md) | Origine dello spazio oggetti per il raggio corrente. |
| [**ObjectRayDirection**](objectraydirection.md) | Direzione dello spazio oggetto per il raggio corrente. |
| [**ObjectToWorld3x4**](objecttoworld3x4.md) | Matrice per la trasformazione dallo spazio oggetti allo spazio globale. |
| [**ObjectToWorld4x3**](objecttoworld4x3.md) | Matrice per la trasformazione dallo spazio oggetti allo spazio globale. |
| [**WorldToObject3x4**](worldtoobject3x4.md) | Matrice per la trasformazione dallo spazio globale allo spazio oggetti |
| [**WorldToObject4x3**](worldtoobject4x3.md) | Matrice per la trasformazione dallo spazio globale allo spazio oggetti |
### <a name="hit-specific-system-values"></a>Valori di sistema specifici dei hit

| Argomento | Descrizione |
|-|-|
| [**HitKind**](hitkind.md) | Restituisce il valore passato come parametro **HitKind** a [**ReportHit.**](reporthit-function.md) |

## <a name="related-topics"></a>Argomenti correlati

* [Informazioni di riferimento di base](direct3d-12-core-reference.md)
* [Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)
