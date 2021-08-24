---
title: setp_comp - vs
description: Impostare il registro predicati. | setp_comp - vs
ms.assetid: bfead3f8-f7fe-4fc1-939f-8e5fbc3e0adf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 892acf44000e178e7ed6774a3841760db32e3ced4d8348a7f9e9c22969bf9024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671771"
---
# <a name="setp_comp---vs"></a>setp \_ comp - vs

Impostare il registro predicati.

## <a name="syntax"></a>Sintassi



| setp \_ comp dst, src0, src1 |
|----------------------------|



 

Dove:

-   \_comp è un confronto per canale tra i due registri di origine. I possibili valori sono i seguenti: 

    | Sintassi | Confronto            |
    |--------|-----------------------|
    | \_Gt   | Maggiore di          |
    | \_Tenente   | Minore di             |
    | \_Ge   | Maggiore o uguale a |
    | \_le   | Minore o uguale a    |
    | \_Eq   | Uguale a              |
    | \_ne   | Diverso da          |

    

     

-   dst è il [registro del registro predicati,](dx9-graphics-reference-asm-vs-registers-predicate.md) p0.
-   src0 è un registro di origine.
-   src1 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| setp \_ comp             |      |      | x    | x     | x    | x     |



 

Questa istruzione funziona come:


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



Per ogni canale che può essere scritto in base alla maschera di scrittura di destinazione, salvare il risultato booleano dell'operazione di confronto tra i canali corrispondenti di src0 e src1 (dopo la risoluzione degli swizzle del modificatore di origine).

I registri di origine consentono l'irruzione arbitraria dei componenti.

Il registro di destinazione consente maschere di scrittura arbitrarie.

Il registro dest deve essere il registro predicato.

## <a name="applying-the-predicate-register"></a>Applicazione del registro predicati

Dopo l'inizializzazione con setp, il registro predicato può essere usato per controllare un'istruzione per componente. Di seguito è illustrata la sintassi:


```
([!]p0[.swizzle]) instruction dest, srcReg, ...
```



Dove:

-   \[!\] è un valore booleano facoltativo NOT
-   p0 è il registro predicato
-   \[.swizzle è uno swizzle facoltativo da applicare al contenuto del registro predicato prima di usarlo \] per mascherare l'istruzione. Gli swizzle disponibili sono: .xyzw (impostazione predefinita se non specificata) o qualsiasi swizzle di replica: .x/.r, .y/.g, .z/.b o .a/.w.
-   l'istruzione è qualsiasi istruzione aritmetica o trama. Non può trattarsi di un'istruzione statica o dinamica di controllo del flusso.
-   dest, srcReg, ... sono i registri richiesti dall'istruzione

Supponendo che il registro predicato sia stato configurato con i valori del componente (true, true, false, false), può essere applicato a questa istruzione:


```
// given r0 = 0,0,1,1
// given r1 = 1,1,0,0
setp_le p0, r0, r1
(p0) add r2, r3, r4
```



per eseguire un'aggiunta di 2 componenti.


```
r2.x = r3.x + r4.x
r2.y = r3.y + r4.y
```



I componenti x e y di r2 non verranno scritti perché il registro predicato conteneva false nei componenti z e w.

L'applicazione del registro predicato a un'istruzione aritmetica o di trama aumenta il conteggio degli slot di istruzioni di 1.

Il registro predicato può essere applicato anche a se [pred - vs](if-pred---vs.md), [callnz pred - vs](callnz-pred---vs.md) e [breakp - vs](breakp---vs.md) instructions. Queste istruzioni di controllo del flusso non hanno alcun aumento del numero di slot di istruzioni quando si usa il registro predicati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




