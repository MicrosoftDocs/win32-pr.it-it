---
title: setp_comp - ps
description: Impostare il registro predicati. | setp_comp - ps
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d278a6104a6c47d84623b185f78b921d61899f296eeaa557a6c6c6d5344097b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119487081"
---
# <a name="setp_comp---ps"></a>setp \_ comp - ps

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

    

     

-   dst è il [registro del registro predicati,](dx9-graphics-reference-asm-ps-registers-predicate.md) p0.
-   src0 è un registro di origine.
-   src1 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| setp \_ comp            |      |      |      |      |      | x    | x     | x    | x     |



 

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

Il registro dst deve essere il registro predicato.

## <a name="applying-the-predicate-register"></a>Applicazione del registro predicati

Dopo che il registro predicato è stato inizializzato con setp comp, può essere usato per controllare \_ un'istruzione per componente. Di seguito è illustrata la sintassi:


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



Dove:

-   \[!\] è un valore booleano facoltativo NOT
-   p0 è il registro predicato
-   \[.swizzle è uno swizzle facoltativo da applicare al contenuto del registro predicato prima di usarlo \] per mascherare l'istruzione. Gli swizzle disponibili sono: .xyzw (impostazione predefinita se non specificata) o qualsiasi swizzle di replica: .x/.r, .y/.g, .z/.b o .a/.w.
-   l'istruzione è qualsiasi istruzione aritmetica o trama. Non può trattarsi di un'istruzione statica o dinamica di controllo del flusso.
-   dest, src0, ... sono i registri richiesti dall'istruzione

Supponendo che il registro predicato sia stato configurato con i valori del componente (true, true, false, false), può essere applicato a questa istruzione:


```
(p0) add r1, r2, r3
```



per eseguire un'aggiunta di 2 componenti.


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



I componenti z e w di r1 non verranno scritti perché il registro predicato conteneva false nei componenti z e w.

L'applicazione del registro predicato a un'istruzione aritmetica o di trama aumenta il conteggio degli slot di istruzioni di 1.

Il registro predicato può essere applicato anche alle istruzioni [pred - ps](if-pred---ps.md), [callnz pred - ps](callnz-pred---ps.md) e [breakp - ps.](break-p---ps.md) Queste istruzioni di controllo del flusso non hanno alcun aumento del numero di slot di istruzioni quando si usa il registro predicati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




