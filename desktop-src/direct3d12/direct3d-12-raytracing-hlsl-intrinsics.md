---
title: Oggetti intrinseci HLSL raytracing Direct3D 12
description: Gli shader HLSL seguenti supportano la pipeline raytracing di Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b2e7cc7053705bd66b37d91f3ee06a6a1f249a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298389"
---
# <a name="raytracing-hlsl-intrinsics"></a>Funzioni intrinseche HLSL raytracing

Le funzioni HLSL intrinisc seguenti supportano la pipeline Direct3D 12 raytracing. 

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento | Descrizione |
|-|-|
| [**AcceptHitAndEndSearch (funzione)**](accepthitandendsearch-function.md) | Usato in un qualsiasi hit shader per confermare l'hit corrente e quindi arrestare la ricerca di altri riscontri per il raggio. |
| [**CallShader (funzione)**](callshader-function.md) | Richiama un altro shader dall'interno di uno shader. |
| [**IgnoreHit (funzione)**](ignorehit-function.md) | Chiamato da un qualsiasi hit shader per rifiutare l'hit e terminare lo shader. |
| [**PrimitiveIndex (funzione)**](primitiveindex.md) | Recupera l'indice generato automaticamente della primitiva all'interno della geometria all'interno dell'istanza della struttura di accelerazione di livello inferiore. |
| [**ReportHit (funzione)**](reporthit-function.md) | Chiamato da un'intersezione shader per segnalare un'intersezione del raggio. |
| [**TraceRay (funzione)**](traceray-function.md) | Invia un raggio in una ricerca di riscontri in una struttura di accelerazione. |

## <a name="related-topics"></a>Argomenti correlati

* [Riferimento principale](direct3d-12-core-reference.md)
* [Guida di riferimento a Direct3D 12](direct3d-12-reference.md)
