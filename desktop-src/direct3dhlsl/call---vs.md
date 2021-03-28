---
title: Call-vs
description: Esegue una chiamata di funzione all'istruzione contrassegnata con l'etichetta fornita. | Call-vs
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c797e7ef6745f5710752fe059d2a2ff1f94a8aa3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969280"
---
# <a name="call---vs"></a>Call-vs

Esegue una chiamata di funzione all'istruzione contrassegnata con l'etichetta fornita.

## <a name="syntax"></a>Sintassi



| chiama l\# |
|----------|



 

dove l \# è un' [etichetta-vs](label---vs.md) che contrassegna l'inizio della subroutine da chiamare.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| chiamare                   |      | x    | x    | x     | x    | x     |



 

Questa istruzione esegue le operazioni seguenti:

1.  Indirizzo push dell'istruzione successiva allo stack di indirizzi restituito.
2.  Continua l'esecuzione dall'istruzione contrassegnata dall'etichetta.

In vertex shader 2 \_ 0 non sono consentite chiamate di annidamento.

In vertex shader 2 \_ x la profondità di annidamento è limitata dall'elemento StaticFlowControlDepth della struttura [**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) . Per ulteriori informazioni, vedere [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).

In vertex shader 3 \_ 0 sono consentiti quattro livelli di annidamento delle chiamate.

Sono consentite solo chiamate in diretta. Ciò significa che la posizione dell'etichetta all'interno del vertex shader deve essere successiva all'istruzione di chiamata a cui fa riferimento.

Se un'istruzione di chiamata viene richiamata all'interno del [ciclo](loop---vs.md)... [EndLoop](endloop---vs.md) Block, il valore del [registro del contatore di cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) è accessibile all'interno della subroutine.

Se una subroutine fa riferimento al [registro del contatore di cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) che si trova all'esterno della subroutine, ogni istanza della chiamata a questa subroutine dovrebbe essere racchiusa da un [ciclo](loop---vs.md)... blocco [EndLoop](endloop---vs.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
