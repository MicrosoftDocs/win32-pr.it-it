---
title: Oggetti intrinseci del valore di sistema di Direct3D 12 raytracing HLSL
description: Gli shader HLSL seguenti supportano la pipeline raytracing di Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a20282e7bc0e9e4898fd361b0959cd6b6f32253
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2020
ms.locfileid: "106300642"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a>Oggetti intrinseci del valore di sistema di Direct3D 12 raytracing HLSL

I valori di sistema vengono recuperati usando funzioni intrinseche speciali, anziché includere parametri con semantica speciale nella firma della funzione shader. 

## <a name="in-this-section"></a>Contenuto della sezione

### <a name="ray-dispatch-system-values"></a>Valori del sistema ray dispatch

| Argomento | Descrizione |
|-|-|
| [**DispatchRaysIndex**](dispatchraysindex.md) | Ottiene la posizione x e y corrente all'interno della larghezza e dell'altezza ottenuta con il valore intrinseco di sistema **DispatchRaysDimensions** . |
| [**DispatchRaysDimensions**](dispatchraysdimensions.md) | I valori di larghezza, altezza e profondità della struttura **D3D12 di \_ distribuzione dei \_ raggi \_** di recapito specificata nella chiamata **DispatchRays** di origine. |

### <a name="ray-system-values"></a>Valori del sistema ray

| Argomento | Descrizione |
|-|-|
| [**WorldRayOrigin**](worldrayorigin.md) | Origine dello spazio globale del raggio corrente. |
| [**WorldRayDirection**](worldraydirection.md) | Direzione dello spazio globale per il raggio corrente. |
| [**RayTMin**](raytmin.md) | Float che rappresenta il punto di partenza parametrico corrente per il raggio. |
| [**RayTCurrent**](raytcurrent.md) | Valore float che rappresenta il punto finale parametrico corrente per il raggio.  |
| [**RayFlags**](rayflags.md) | Unsigned Integer contenente i flag di **ray_flag** correnti. |

### <a name="primitiveobject-space-system-values"></a>Valori di sistema per spazio oggetti/primitivi

| Argomento | Descrizione |
|-|-|
| [**InstanceIndex**](instanceindex.md) | Indice generato automaticamente dell'istanza corrente nella struttura di accelerazione raytracing di primo livello. |
| [**InstanceID**](instanceid.md) | Identificatore fornito dall'utente per l'istanza nell'istanza della struttura di accelerazione di livello inferiore all'interno della struttura di primo livello. |
| [**PrimitiveIndex**](primitiveindex.md) | Indice generato automaticamente della primitiva all'interno della geometria all'interno dell'istanza della struttura di accelerazione di livello inferiore. |
| [**ObjectRayOrigin**](objectrayorigin.md) | Origine dello spazio oggetto per il raggio corrente. |
| [**ObjectRayDirection**](objectraydirection.md) | Direzione dello spazio dell'oggetto per il raggio corrente. |
| [**ObjectToWorld3x4**](objecttoworld3x4.md) | Matrice per la trasformazione dallo spazio oggetto allo spazio globale. |
| [**ObjectToWorld4x3**](objecttoworld4x3.md) | Matrice per la trasformazione dallo spazio oggetto allo spazio globale. |
| [**WorldToObject3x4**](worldtoobject3x4.md) | Matrice per la trasformazione da spazio globale a oggetto-spazio |
| [**WorldToObject4x3**](worldtoobject4x3.md) | Matrice per la trasformazione da spazio globale a oggetto-spazio |
### <a name="hit-specific-system-values"></a>Valori di sistema specifici di hit

| Argomento | Descrizione |
|-|-|
| [**HitKind**](hitkind.md) | Restituisce il valore passato come parametro **HitKind** a [**ReportHit**](reporthit-function.md). |

## <a name="related-topics"></a>Argomenti correlati

* [Riferimento principale](direct3d-12-core-reference.md)
* [Guida di riferimento a Direct3D 12](direct3d-12-reference.md)
