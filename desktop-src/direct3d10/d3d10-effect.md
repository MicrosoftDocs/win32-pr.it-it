---
description: Queste costanti vengono usate durante la creazione di un effetto per definire il comportamento di compilazione o di effetto di runtime.
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: D3D10_EFFECT costanti
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e3738a95a843020f7c0f8af30e8c5d035f0a86ac7098d36cae422eb01ed4dc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736050"
---
# <a name="d3d10_effect-constants"></a>Costanti EFFECT D3D10 \_

Queste costanti vengono usate durante la creazione di un effetto per definire il comportamento di compilazione o di effetto di runtime.



| \#Definire                                 | Valore        | Descrizione                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EFFETTO D3D10 \_ \_ COMPILE CHILD \_ \_ EFFECT    | 1 << 0 | Compilare il file con estensione fx con un effetto figlio. Gli effetti figlio non hanno inizializzazioni per i valori condivisi perché vengono inizializzati nel pool di effetti.                                                                                                           |
| LA COMPILAZIONE DELL'EFFETTO D3D10 \_ \_ CONSENTE OPERAZIONI \_ \_ \_ LENTE | 1 << 1 | Per impostazione predefinita, la modalità prestazioni è abilitata. La modalità prestazioni impedisce la visualizzazione di oggetti di stato modificabili impedendo la visualizzazione di espressioni non letterali nelle definizioni degli oggetti di stato. Se si specifica questo flag, la modalità verrà disabilitata e gli oggetti di stato modificabili saranno consentiti. |
| EFFETTO D3D10 \_ \_ A THREAD \_ SINGOLO          | 1 << 3 | Non tentare di eseguire la sincronizzazione con altri effetti di caricamento dei thread nello stesso pool.                                                                                                                                                                        |



 

Queste costanti sono definite come macro in d3d10effect.h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Effect (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



