---
title: call - vs
description: Esegue una chiamata di funzione all'istruzione contrassegnata con l'etichetta fornita. | call - vs
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d2321224b10ca1f7822b19e48ebbb58c1e01c261720f64a8b39331fbceab75fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986891"
---
# <a name="call---vs"></a>call - vs

Esegue una chiamata di funzione all'istruzione contrassegnata con l'etichetta fornita.

## <a name="syntax"></a>Sintassi



| call l\# |
|----------|



 

dove l \# è [un'etichetta e contrassegna](label---vs.md) l'inizio della subroutine da chiamare.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| chiamare                   |      | x    | x    | x     | x    | x     |



 

Questa istruzione esegue le operazioni seguenti:

1.  Indirizzo push dell'istruzione successiva nello stack di indirizzi mittente.
2.  Continuare l'esecuzione dall'istruzione contrassegnata dall'etichetta .

Nel vertex shader 2 \_ 0 le chiamate di annidamento non sono consentite.

Nel vertex shader 2 x la profondità di annidamento è limitata dall'elemento \_ StaticFlowControlDepth della [**struttura D3DVSHADERCAPS2 \_ 0.**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) Per altre informazioni, vedere [**GetDeviceCaps.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps)

Nel vertex shader 3 \_ 0 sono consentiti quattro livelli di annidamento delle chiamate.

Sono consentite solo chiamate di inoltro. Ciò significa che la posizione dell'etichetta all'interno del vertex shader deve essere dopo l'istruzione di chiamata che fa riferimento a essa.

Se un'istruzione di chiamata viene richiamata all'interno [del ciclo](loop---vs.md)... [endloop](endloop---vs.md) block, il valore di [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) è accessibile all'interno della subroutine.

Se una subroutine fa [](dx9-graphics-reference-asm-vs-registers-loop-counter.md) riferimento al registro dei contatori dei cicli (aL) che si trova all'esterno della subroutine, ogni istanza della chiamata a questa subroutine deve essere racchiusa da un [ciclo](loop---vs.md)... [blocco endloop.](endloop---vs.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
