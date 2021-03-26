---
title: Registro di origine swizzling (HLSL VS Reference)
description: Prima dell'esecuzione di un'istruzione, i dati in un registro di origine vengono copiati in un registro temporaneo. Swizzling si riferisce alla possibilità di copiare qualsiasi componente del registro di origine in qualsiasi componente di registro temporaneo. Swizzling non influisce sui dati del registro di origine.
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c075d8ff47b1f76adf378b6a583cd4d675651a87
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104398324"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a>Registro di origine swizzling (HLSL VS Reference)

Prima dell'esecuzione di un'istruzione, i dati in un registro di origine vengono copiati in un registro temporaneo. Swizzling si riferisce alla possibilità di copiare qualsiasi componente del registro di origine in qualsiasi componente di registro temporaneo. Swizzling non influisce sui dati del registro di origine.

## <a name="component-swizzling"></a>Swizzling componente

Come illustrato nella tabella seguente, è possibile applicare swizzling ai singoli componenti dei dati del registro di origine (dove sono uno dei registri di input del vertex shader validi [-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).



| Modificatore Component                 | Descrizione    |
|------------------------------------|----------------|
| r. \[ xyzw \] \[ xyzw \] \[ xyzw \] \[ xyzw\] | Swizzle di origine |



 

-   Tutti e quattro i componenti vengono sempre copiati. Se si specificano meno di quattro componenti, l'ultimo componente viene ripetuto (XY indica. XYYY). Se non viene specificato alcun componente, x viene ripetuto (. xxxx).
-   I componenti possono essere visualizzati in qualsiasi ordine. V0. ywx restituisce V0. ywxx.
-   I componenti RGBA possono essere utilizzati rispettivamente per xyzw (r per x, g per b e così via).
-   Queste istruzioni implementano il componente singolo del registro di origine swizzles: EXP, EXPP, log, LogP, POW, RCP, RSQ. Il risultato di queste istruzioni viene copiato in tutti e quattro i componenti del registro di destinazione.

Non è possibile usare swizzling nelle istruzioni [M3X2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [m4x3-vs](m4x3---vs.md)e [M4x4-vs](m4x4---vs.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




