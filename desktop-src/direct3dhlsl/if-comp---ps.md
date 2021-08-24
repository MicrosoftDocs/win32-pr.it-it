---
title: if_comp - ps
description: 'Avviare un if bool - ps... else - ps... endif : blocco ps, con una condizione basata su valori che possono essere calcolati in uno shader. Questa istruzione viene usata per ignorare un blocco di codice, in base a una condizione.'
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5d0a2271dbd67902a039ddadf585611ed98fdb115f468c3962baa8cb46f48508
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788971"
---
# <a name="if_comp---ps"></a>if \_ comp - ps

Avviare un [if bool - ps](if-bool---ps.md)... [else - ps](else---ps.md)... [endif : blocco ps,](endif---ps.md) con una condizione basata su valori che possono essere calcolati in uno shader. Questa istruzione viene usata per ignorare un blocco di codice, in base a una condizione.

## <a name="syntax"></a>Sintassi



| se \_ comp src0, src1 |
|---------------------|



 

Dove:

-   \_comp è un confronto tra i due registri di origine. I possibili valori sono i seguenti: 

    | Sintassi | Confronto            |
    |--------|-----------------------|
    | \_Gt   | Maggiore di          |
    | \_Tenente   | Minore di             |
    | \_Ge   | Maggiore o uguale a |
    | \_le   | Minore o uguale a    |
    | \_Eq   | Uguale a              |
    | \_ne   | Diverso da          |

    

     

-   src0 è un registro di origine. Lo swizzle di replica è necessario per selezionare un componente.
-   src1 è un registro di origine. Lo swizzle di replica è necessario per selezionare un componente.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| if \_ comp              |      |      |      |      |      | x    | x     | x    | x     |



 

Questa istruzione viene usata per ignorare un blocco di codice, in base a una condizione.


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



Prestare attenzione all'uso delle modalità di confronto uguale a e non uguale a nei numeri a virgola mobile. Poiché l'arrotondamento si verifica durante i calcoli a virgola mobile, il confronto può essere eseguito con un valore epsilon (numero piccolo diverso da zero) per evitare errori.

Tali restrizioni includono:

-   if \_ comp... [else - ps](else---ps.md)... [endif: i blocchi ps](endif---ps.md) (insieme ai blocchi [if](if-bool---ps.md) predicati) possono essere annidati fino a 24 livelli di profondità.
-   I registri src0 e src1 richiedono uno swizzle di replica.
-   se \_ i blocchi comp devono terminare con [un'istruzione else , vs](else---vs.md) o [endif.](endif---vs.md)
-   if \_ comp... [else - ps](else---ps.md)... [endif: i blocchi ps](endif---ps.md) non possono essere in un blocco di ciclo. Il blocco if \_ comp deve essere completamente all'interno o all'esterno del blocco di ciclo.

## <a name="example"></a>Esempio

Questa istruzione fornisce il controllo dinamico condizionale del flusso.


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




