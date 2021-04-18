---
description: Queste costanti si applicano alle variabili di effetto.
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: Costanti D3D10_EFFECT_VARIABLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6367fe89f66ff90991b8493a03a6d1b4244f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304718"
---
# <a name="d3d10_effect_variable-constants"></a>Costanti della variabile di \_ effetto D3D10 \_

Queste costanti si applicano alle variabili di effetto.



| \#definire                                       | Descrizione  | Valore                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ Annotazione variabile effetto D3D10 \_            | 1 << 0 | Indica che si tratta di un'annotazione o una variabile globale.                                                                                                                                                                                                        |
| \_Variabile effetto d3d10 in \_ \_ pool                | 1 << 1 | Indica che la variabile o il buffer costante si trova in un pool di effetti. Se questo flag non è impostato, la variabile si trova in un effetto autonomo o un effetto figlio (gli effetti autonomi restituiscono false da [**ID3D10Effect:: il pool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool). |
| \_Punto di \_ \_ Binding esplicito variabile \_ effetto D3D10 \_ | 1 << 2 | Indica che la variabile è stata associata in modo esplicito tramite la parola chiave register.                                                                                                                                                                                 |



 

Questi flag sono definiti come macro in d3d10effect. h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti effetto (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



