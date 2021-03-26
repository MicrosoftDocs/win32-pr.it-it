---
title: setp_comp-PS
description: Impostare il registro del predicato. | setp_comp-PS
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a68da290ecb04e9cb7ae49c5525997fbf4c112a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234826"
---
# <a name="setp_comp---ps"></a>setp \_ comp-PS

Impostare il registro del predicato.

## <a name="syntax"></a>Sintassi



| setp \_ comp DST, src0, src1 |
|----------------------------|



 

Dove:

-   \_comp è un confronto per canale tra i due registri di origine. I possibili valori sono i seguenti: 

    | Sintassi | Confronto            |
    |--------|-----------------------|
    | \_gt   | Maggiore di          |
    | \_lt   | Minore di             |
    | \_GE   | Maggiore o uguale a |
    | \_le   | Minore o uguale a    |
    | \_EQ   | Uguale a              |
    | \_ne   | Diverso da          |

    

     

-   DST è il registro [Register del predicato](dx9-graphics-reference-asm-ps-registers-predicate.md) , P0.
-   src0 è un registro di origine.
-   src1 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| setp \_ comp            |      |      |      |      |      | x    | x     | x    | x     |



 

Questa istruzione funziona come segue:


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



Per ogni canale che può essere scritto in base alla maschera di scrittura di destinazione, salvare il risultato booleano dell'operazione di confronto tra i canali corrispondenti di src0 e src1 (dopo la risoluzione del modificatore di origine swizzles).

I registri di origine consentono di specificare un componente arbitrario swizzles.

Il registro di destinazione consente le maschere di scrittura arbitrarie.

Il registro DST deve essere il registro predicato.

## <a name="applying-the-predicate-register"></a>Applicazione del registro predicato

Quando il registro predicato è stato inizializzato con setp \_ comp, può essere usato per controllare un'istruzione per ogni componente. Ecco la sintassi:


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



Dove:

-   \[!\] è un valore booleano facoltativo NOT
-   P0 è il registro predicato
-   \[. Swizzle \] è un swizzle facoltativo da applicare al contenuto del registro predicato prima di utilizzarlo per mascherare l'istruzione. I swizzles disponibili sono:. xyzw (impostazione predefinita quando non è specificato alcun parametro) o qualsiasi replica swizzle:. x/. r,. y/. g,. z/. b o. a/. w.
-   l'istruzione è qualsiasi aritmetic o istruzione di trama. Non può essere un'istruzione di controllo di flusso statica o dinamica.
-   dest, src0,... sono i registri richiesti dall'istruzione

Supponendo che il registro dei predicati sia stato configurato con i valori dei componenti (true, true, false, false), è possibile applicare questa istruzione:


```
(p0) add r1, r2, r3
```



per eseguire un'aggiunta a 2 componenti.


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



I componenti z e w di R1 non verranno scritti poiché il registro predicato contiene false nei componenti z e w.

Se si applica il registro predicato a un'istruzione aritmetica o di trama, il numero di slot di istruzioni aumenta di 1.

Il registro predicato può essere applicato anche a se le istruzioni [prede-PS](if-pred---ps.md), [callnz prede-PS](callnz-pred---ps.md) e [Breakp-PS](break-p---ps.md) . Queste istruzioni di controllo di flusso non hanno alcun aumento nel numero di slot di istruzioni quando si usa il registro predicato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




