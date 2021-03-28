---
title: texbeml-PS
description: Applicare una trasformazione della mappa dell'ambiente di Bump Fake con la correzione della luminanza. Questa operazione viene eseguita modificando i dati dell'indirizzo di trama del registro di destinazione, usando i dati di risoluzione dell'indirizzo (du, DV), una matrice di ambiente Bump 2D e la luminanza.
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d97877c67970f43a995fcfbe21d9aead2d792e09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963408"
---
# <a name="texbeml---ps"></a>texbeml-PS

Applicare una trasformazione della mappa dell'ambiente di Bump Fake con la correzione della luminanza. Questa operazione viene eseguita modificando i dati dell'indirizzo di trama del registro di destinazione, usando i dati di risoluzione dell'indirizzo (du, DV), una matrice di ambiente Bump 2D e la luminanza.

## <a name="syntax"></a>Sintassi



| texbeml DST, src |
|------------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texbeml               | x    | x    | x    |      |      |      |       |      |       |



 

I dati di colore rosso e verde nel registro src vengono interpretati come dati di perturbazione (du, DV). I dati di colore blu nel registro src vengono interpretati come dati di luminanza.

Questa istruzione trasforma i componenti rosso e verde nel registro di origine usando la matrice di mapping dell'ambiente Bump 2D. Il risultato viene aggiunto al set di coordinate di trama corrispondente al numero di registro di destinazione. Viene applicata una correzione della luminanza usando il valore della luminanza e i valori della fase della trama di distorsione. Il risultato viene usato per campionare la fase di trama corrente.

Questa operazione può essere usata per diverse tecniche in base alla turbativa degli indirizzi, ad esempio il mapping di un ambiente per singolo pixel.

Questa operazione interpreta sempre du e DV come quantità con segno. Per le versioni 1 \_ 0 e 1 \_ 1, il modificatore di input con [segno di ridimensionamento del registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) non è consentito nell'argomento di input.

Questa istruzione genera risultati definiti quando le trame di input contengono dati in formato misto. Per ulteriori informazioni sui formati di superficie, vedere [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



In questo esempio vengono illustrati i calcoli eseguiti nell'istruzione.


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



u ' = TextureCoordinates (fase m)<sub>u</sub> +

D3DTSS \_ BUMPENVMAT00 (fase m) \* t (n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT10 (fase m) \* t (n)<sub>G</sub>

v'= TextureCoordinates (fase m)<sub>v</sub> +

D3DTSS \_ BUMPENVMAT01 (fase m) \* t (n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT11 (fase m) \* t (n)<sub>G</sub>

t (m)<sub>RGBA</sub> = TextureSample (fase m) con (u ', v') come coordinate

t (m)<sub>RGBA</sub> = t (m)<sub>RGBA</sub>\*

\[(t (n)<sub>B</sub> \* D3DTSS \_ BUMPENVLSCALE (fase m)) +

D3DTSS \_ BUMPENVLOFFSET (fase m)\]

I dati che sono stati letti da un'istruzione [texbem](texbem---ps.md) o texbeml non possono essere letti in un secondo momento, ad eccezione di un altro texbem o texbeml.


```
// This example demonstrates the validation error caused by 
//   t0 being reread
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a>Esempio

Di seguito è riportato un esempio di shader con le mappe di trama identificate e le fasi di trama identificate.


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



Questo esempio richiede le seguenti trame nelle fasi di trama seguenti.

-   Alla fase 0 viene assegnata una mappa Bump con i dati di perturbazione (du, DV).
-   Alla fase 1 viene assegnata una mappa di trama con dati di colore.
-   texbeml imposta i dati della matrice nella fase di trama campionata. Si tratta di una differenza rispetto alla funzionalità della pipeline della funzione fissa in cui i dati di perturbazione e le matrici occupano la stessa fase della trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 