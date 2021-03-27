---
title: if_comp-PS
description: Avvia un'if bool-PS... else-PS... il blocco endif-PS, con una condizione basata sui valori che possono essere calcolati in uno shader. Questa istruzione viene usata per ignorare un blocco di codice, in base a una condizione.
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db30983c83bc7d66e06befd07f4eb1dcdc9b21ea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719351"
---
# <a name="if_comp---ps"></a>Se \_ comp-PS

Avvia un' [if bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... il blocco [endif-PS](endif---ps.md) , con una condizione basata sui valori che possono essere calcolati in uno shader. Questa istruzione viene usata per ignorare un blocco di codice, in base a una condizione.

## <a name="syntax"></a>Sintassi



| Se \_ comp src0, src1 |
|---------------------|



 

Dove:

-   \_comp è un confronto tra i due registri di origine. I possibili valori sono i seguenti: 

    | Sintassi | Confronto            |
    |--------|-----------------------|
    | \_gt   | Maggiore di          |
    | \_lt   | Minore di             |
    | \_GE   | Maggiore o uguale a |
    | \_le   | Minore o uguale a    |
    | \_EQ   | Uguale a              |
    | \_ne   | Diverso da          |

    

     

-   src0 è un registro di origine. Per selezionare un componente, è necessario replicare Swizzle.
-   src1 è un registro di origine. Per selezionare un componente, è necessario replicare Swizzle.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Se \_ comp              |      |      |      |      |      | x    | x     | x    | x     |



 

Questa istruzione viene usata per ignorare un blocco di codice, in base a una condizione.


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



Prestare attenzione a usare le modalità di confronto uguale a e non uguale per i numeri a virgola mobile. Poiché l'arrotondamento si verifica durante i calcoli a virgola mobile, il confronto può essere eseguito su un valore Epsilon (un numero diverso da zero) per evitare errori.

Tali restrizioni includono:

-   Se \_ comp... [else-PS](else---ps.md)... i blocchi [endif-PS](endif---ps.md) (insieme ai blocchi [if](if-bool---ps.md) predicati) possono essere annidati fino a 24 livelli di profondità.
-   i registri src0 e src1 richiedono una replica Swizzle.
-   Se i \_ blocchi comp devono terminare con un'istruzione [else-vs](else---vs.md) o [endif-vs](endif---vs.md) .
-   Se \_ comp... [else-PS](else---ps.md)... i blocchi [endif-PS](endif---ps.md) non possono risiedere in un blocco di ciclo. Il \_ blocco If comp deve trovarsi completamente all'interno o all'esterno del blocco del ciclo.

## <a name="example"></a>Esempio

Questa istruzione fornisce il controllo di flusso dinamico condizionale.


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




