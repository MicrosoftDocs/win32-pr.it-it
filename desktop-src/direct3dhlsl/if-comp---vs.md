---
title: if_comp-vs
description: Avviare un if bool-vs... else-vs... il blocco endif-vs, con una condizione basata sui valori che possono essere calcolati in uno shader. Questa istruzione viene usata per ignorare un blocco di codice, in base a una condizione.
ms.assetid: a3fe93c6-be26-4216-a601-3be52a74be06
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadbe9620367efc75f821a711de89eb3498d247f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992960"
---
# <a name="if_comp---vs"></a>Se \_ comp-vs

Avviare un [if bool-vs](if-bool---vs.md)... [else-vs](else---vs.md)... il blocco [endif-vs](endif---vs.md) , con una condizione basata sui valori che possono essere calcolati in uno shader. Questa istruzione viene usata per ignorare un blocco di codice, in base a una condizione.

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



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Se \_ comp               |      |      | x    | x     | x    | x     |



 

Questa istruzione viene usata per ignorare un blocco di codice, in base a una condizione.


```
if_lt src0, src1
   jump to the corresponding else or endif instruction;
```



Prestare attenzione a usare le modalità di confronto uguale a e non uguale per i numeri a virgola mobile. Poiché l'arrotondamento si verifica durante i calcoli a virgola mobile, il confronto può essere eseguito su un valore Epsilon (un numero diverso da zero) per evitare errori.

Tali restrizioni includono:

-   Se \_ comp... [else-vs](else---vs.md)... i blocchi [endif-vs](endif---vs.md) (insieme ai blocchi if predicati) possono essere annidati fino a 24 livelli di profondità.
-   i registri src0 e src1 richiedono una replica Swizzle.
-   Se i \_ blocchi comp devono terminare con un'istruzione [else-vs](else---vs.md) o [endif-vs](endif---vs.md) .
-   Se \_ comp... [else-vs](else---vs.md)... i blocchi [endif-vs](endif---vs.md) non possono risiedere in un blocco di ciclo. Il \_ blocco If comp deve essere completamente interno o all'esterno del blocco [loop-vs](loop---vs.md) .

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

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




