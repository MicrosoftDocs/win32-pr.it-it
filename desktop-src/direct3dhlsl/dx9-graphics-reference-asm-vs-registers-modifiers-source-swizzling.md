---
title: Source Register Swizzling (informazioni di riferimento su HLSL VS)
description: Prima dell'esecuzione di un'istruzione, i dati in un registro di origine vengono copiati in un registro temporaneo. Swizzling si riferisce alla possibilità di copiare qualsiasi componente del registro di origine in qualsiasi componente di registro temporaneo. Lo swizzling non influisce sui dati del registro di origine.
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03dd2d9051c185d1be1ccb6fce18549bf5aa3414975c9a600bb8f8c47f78d4c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854551"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a>Source Register Swizzling (informazioni di riferimento su HLSL VS)

Prima dell'esecuzione di un'istruzione, i dati in un registro di origine vengono copiati in un registro temporaneo. Swizzling si riferisce alla possibilità di copiare qualsiasi componente del registro di origine in qualsiasi componente di registro temporaneo. Lo swizzling non influisce sui dati del registro di origine.

## <a name="component-swizzling"></a>Componente swizzling

Come illustrato nella tabella seguente, la swizzling può essere applicata ai singoli componenti dei dati del registro di origine (dove è uno dei registri di input del vertex shader valido, rispetto a [ \_ 1 \_ 1).](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)



| Modificatore di componente                 | Descrizione    |
|------------------------------------|----------------|
| r. \[ xyzw \] \[ xyzw \] \[ xyzw \] \[ xyzw\] | Swizzle di origine |



 

-   Tutti e quattro i componenti vengono sempre copiati. Se vengono specificati meno di quattro componenti, l'ultimo componente viene ripetuto (xy significa .xyyy). Se non viene specificato alcun componente, x viene ripetuto (.xxxx).
-   I componenti possono essere visualizzati in qualsiasi ordine. v0.ywx risulta in v0.ywxx.
-   I componenti rgba possono essere usati rispettivamente per xyzw (r per x, g per b e così via).
-   Queste istruzioni implementano gli swizzle a componente singolo del registro di origine: exp, expp, log, logp, pow, rcp, rsq. Il risultato di queste istruzioni viene copiato in tutti e quattro i componenti del registro di destinazione.

Non è possibile usare swizzling in [m3x2 ,](m3x2---vs.md)vs , [m3x3 - vs](m3x3---vs.md), [m4x3 - vs](m4x3---vs.md)e [m4x4 - rispetto alle](m4x4---vs.md) istruzioni .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori di registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




