---
title: lit - vs
description: Fornisce supporto parziale per l'illuminazione calcolando i coefficienti di illuminazione da due prodotti punto e un esponente.
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e5b5ff3451424251d778886af3841c673ce5a85d91022db9144c62574c16640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089324"
---
# <a name="lit---vs"></a>lit - vs

Fornisce supporto parziale per l'illuminazione calcolando i coefficienti di illuminazione da due prodotti punto e un esponente.

## <a name="syntax"></a>Sintassi



| lit dst, src |
|--------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Illuminato                    | x    | x    | x    | x     | x    | x     |



 

Si presuppone che il vettore di origine contenga i valori illustrati nello pseudocodice seguente.


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



Il frammento di codice seguente illustra le operazioni eseguite.


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



L'aritmetica con precisione ridotta è accettabile nella valutazione del componente y di destinazione (dest.y). Un'implementazione deve supportare almeno otto bit frazionari nell'argomento power. I prodotti a punti vengono calcolati con vettori normalizzati e i limiti di chiusura sono da -128 a 128.

L'errore deve corrispondere a una combinazione [logp](logp---vs.md) - vs [ed exp -](exp---vs.md) o non più di un bit significativo per un componente a colori a 8 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




