---
description: Queste costanti utilizzate quando si crea un effetto per definire il comportamento di compilazione o l'effetto di Runtime.
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: Costanti D3D10_EFFECT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c12b7a458bb7c97bb53436565513673006a2884
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342161"
---
# <a name="d3d10_effect-constants"></a>\_Costanti effetto D3D10

Queste costanti utilizzate quando si crea un effetto per definire il comportamento di compilazione o l'effetto di Runtime.



| \#definire                                 | Valore        | Descrizione                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ Effetto figlio compilazione effetto \_ D3D10    | 1 << 0 | Compilare il file con estensione FX in un effetto figlio. Gli effetti figlio non hanno inizializzazioni per alcun valore condiviso perché vengono inizializzati nel pool di effetti.                                                                                                           |
| D3D10 \_ effetto \_ compilazione \_ Consenti \_ \_ operazioni lente | 1 << 1 | Per impostazione predefinita, è abilitata la modalità prestazioni. La modalità prestazioni non consente oggetti di stato modificabili impedendo la visualizzazione di espressioni non letterali nelle definizioni degli oggetti di stato. Se si specifica questo flag, verrà disabilitata la modalità e gli oggetti di stato modificabili. |
| D3D10 \_ effetto \_ a \_ thread singolo          | 1 << 3 | Non tentare di eseguire la sincronizzazione con altri thread che caricano effetti nello stesso pool.                                                                                                                                                                        |



 

Queste costanti sono definite come macro in d3d10effect. h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti effetto (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



