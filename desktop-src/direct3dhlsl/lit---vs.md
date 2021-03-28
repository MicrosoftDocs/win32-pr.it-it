---
title: Lit-vs
description: Fornisce un supporto parziale per l'illuminazione calcolando i coefficienti di illuminazione da due prodotti punto e un esponente.
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99c25c377ff6064a704d56b9e7b31d41b37117e5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976394"
---
# <a name="lit---vs"></a>Lit-vs

Fornisce un supporto parziale per l'illuminazione calcolando i coefficienti di illuminazione da due prodotti punto e un esponente.

## <a name="syntax"></a>Sintassi



| Lit DST, src |
|--------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| acceso                    | x    | x    | x    | x     | x    | x     |



 

Si presuppone che il vettore di origine contenga i valori mostrati nello pseudocodice seguente.


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



Nel frammento di codice seguente vengono illustrate le operazioni eseguite.


```
dest.x = 1;
dest.y = 0;
dest.z = 0;
dest.w = 1;

float power = src.w;
const float MAXPOWER = 127.9961f;
if (power < -MAXPOWER)
    power = -MAXPOWER;          // Fits into 8.8 fixed point format
else if (power > MAXPOWER)
    power = MAXPOWER;          // Fits into 8.8 fixed point format

if (src.x > 0)
{
    dest.y = src.x;
    if (src.y > 0)
    {
        // Allowed approximation is EXP(power * LOG(src.y))
        dest.z = (float)(pow(src.y, power));
    }
}
```



L'aritmetica a precisione ridotta è accettabile per la valutazione del componente y di destinazione (dest. y). Un'implementazione di deve supportare almeno otto bit di frazione nell'argomento di risparmio energia. I prodotti dot vengono calcolati con vettori normalizzati e i limiti di clamp sono da-128 a 128.

È necessario che l'errore corrisponda a una combinazione di [LogP-vs](logp---vs.md) e [Exp-vs](exp---vs.md) oppure non più di circa un bit significativo per un componente colore a 8 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




