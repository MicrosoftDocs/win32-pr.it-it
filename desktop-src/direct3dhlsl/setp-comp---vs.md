---
title: setp_comp-vs
description: Impostare il registro del predicato. | setp_comp-vs
ms.assetid: bfead3f8-f7fe-4fc1-939f-8e5fbc3e0adf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77d9e5f46e9fb8bbcfb96e56d13cd6f7cebfecc2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104401888"
---
# <a name="setp_comp---vs"></a>setp \_ comp-vs

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

    

     

-   DST è il registro [Register del predicato](dx9-graphics-reference-asm-vs-registers-predicate.md) , P0.
-   src0 è un registro di origine.
-   src1 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| setp \_ comp             |      |      | x    | x     | x    | x     |



 

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

Il registro dest deve essere il registro predicato.

## <a name="applying-the-predicate-register"></a>Applicazione del registro predicato

Una volta inizializzato il registro predicato con setp, è possibile usarlo per controllare un'istruzione per ogni componente. Ecco la sintassi:


```
([!]p0[.swizzle]) instruction dest, srcReg, ...
```



Dove:

-   \[!\] è un valore booleano facoltativo NOT
-   P0 è il registro predicato
-   \[. Swizzle \] è un swizzle facoltativo da applicare al contenuto del registro predicato prima di utilizzarlo per mascherare l'istruzione. I swizzles disponibili sono:. xyzw (impostazione predefinita quando non è specificato alcun parametro) o qualsiasi replica swizzle:. x/. r,. y/. g,. z/. b o. a/. w.
-   l'istruzione è qualsiasi aritmetic o istruzione di trama. Non può essere un'istruzione di controllo di flusso statica o dinamica.
-   dest, srcReg,... sono i registri richiesti dall'istruzione

Supponendo che il registro dei predicati sia stato configurato con i valori dei componenti (true, true, false, false), è possibile applicare questa istruzione:


```
// given r0 = 0,0,1,1
// given r1 = 1,1,0,0
setp_le p0, r0, r1
(p0) add r2, r3, r4
```



per eseguire un'aggiunta a 2 componenti.


```
r2.x = r3.x + r4.x
r2.y = r3.y + r4.y
```



I componenti x e y di R2 non verranno scritti poiché il registro predicato contiene false nei componenti z e w.

Se si applica il registro predicato a un'istruzione aritmetica o di trama, il numero di slot di istruzioni aumenta di 1.

Il registro predicato può essere applicato anche a se le istruzioni [prede-vs](if-pred---vs.md), [callnz prede-vs](callnz-pred---vs.md) e [Breakp-vs](breakp---vs.md) . Queste istruzioni di controllo di flusso non hanno alcun aumento nel numero di slot di istruzioni quando si usa il registro predicato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




