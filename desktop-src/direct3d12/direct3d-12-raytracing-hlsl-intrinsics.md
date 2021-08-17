---
title: Oggetti intrinseci HLSL raytracing di Direct3D 12
description: Visualizzare i collegamenti agli articoli che descrivono le funzioni intrinseche HLSL (High-Level Shader Language) che supportano la pipeline di raytracing Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce12f90233dee05bb4959498d3cb366aa88f1140182384bc26f5b017ee2bf64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733784"
---
# <a name="raytracing-hlsl-intrinsics"></a>Funzioni intrinseche HLSL di raytracing

Le funzioni di intrinisc HLSL seguenti supportano la pipeline di raytracing Direct3D 12. 

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento | Descrizione |
|-|-|
| [**Funzione AcceptHitAndEndSearch**](accepthitandendsearch-function.md) | Usato in un hit shader per eseguire il commit dell'hit corrente e quindi interrompere la ricerca di altri riscontri per il raggio. |
| [**Funzione CallShader**](callshader-function.md) | Richiama un altro shader dall'interno di uno shader. |
| [**Funzione IgnoreHit**](ignorehit-function.md) | Chiamato da un hit shader per rifiutare l'hit e terminare lo shader. |
| [**Funzione PrimitiveIndex**](primitiveindex.md) | Recupera l'indice rigenerato automaticamente della primitiva all'interno della geometria all'interno dell'istanza della struttura di accelerazione di livello inferiore. |
| [**Funzione ReportHit**](reporthit-function.md) | Chiamato da uno shader di intersezione per segnalare un'intersezione di raggi. |
| [**Funzione TraceRay**](traceray-function.md) | Invia un raggio in una ricerca di riscontri in una struttura di accelerazione. |

## <a name="related-topics"></a>Argomenti correlati

* [Informazioni di riferimento di base](direct3d-12-core-reference.md)
* [Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)
