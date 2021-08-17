---
description: Queste costanti si applicano alle variabili di effetto.
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: D3D10_EFFECT_VARIABLE costanti
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7541253fffd6671e01a8da38c06fd15924d45b461d5acc0e468fd17660746f42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736070"
---
# <a name="d3d10_effect_variable-constants"></a>Costanti D3D10 \_ EFFECT \_ VARIABLE

Queste costanti si applicano alle variabili di effetto.



| \#Definire                                       | Descrizione  | Valore                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ANNOTAZIONE DELLA VARIABILE \_ DELL'EFFETTO D3D10 \_ \_            | 1 << 0 | Indica che si tratta di un'annotazione o di una variabile globale.                                                                                                                                                                                                        |
| VARIABILE DELL'EFFETTO D3D10 \_ \_ IN \_ POOL                | 1 << 1 | Indica che la variabile o il buffer costante si trova in un pool di effetti. Se questo flag non è impostato, la variabile risiede in un effetto autonomo o in un effetto figlio (gli effetti autonomi restituiscono false da [**ID3D10Effect::IsPool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool). |
| PUNTO DI ASSOCIAZIONE \_ ESPLICITO DELLA \_ VARIABILE DI EFFETTO \_ \_ \_ D3D10 | 1 << 2 | Indica che la variabile è stata associata in modo esplicito usando la parola chiave register.                                                                                                                                                                                 |



 

Questi flag sono definiti come macro in d3d10effect.h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti degli effetti (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



