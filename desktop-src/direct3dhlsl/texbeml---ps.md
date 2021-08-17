---
title: texbeml - ps
description: Applicare una trasformazione della mappa dell'ambiente di urti fittizia con correzione della luminanza. Questa operazione viene eseguita modificando i dati dell'indirizzo di trama del registro di destinazione, usando i dati di perturbazione degli indirizzi (du,dv), una matrice dell'ambiente di urto 2D e la luminanza.
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c549e93829c3165d4921342d4e74a8dc15bc1518f7c88aa205f8afc889fae95e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788065"
---
# <a name="texbeml---ps"></a>texbeml - ps

Applicare una trasformazione della mappa dell'ambiente di urti fittizia con correzione della luminanza. Questa operazione viene eseguita modificando i dati dell'indirizzo di trama del registro di destinazione, usando i dati di perturbazione degli indirizzi (du,dv), una matrice dell'ambiente di urto 2D e la luminanza.

## <a name="syntax"></a>Sintassi



| texbeml dst, src |
|------------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texbeml               | x    | x    | x    |      |      |      |       |      |       |



 

I dati di colore rosso e verde nel registro src vengono interpretati come dati di perturbazione (du,dv). I dati di colore blu nel registro src vengono interpretati come dati di luminanza.

Questa istruzione trasforma i componenti rosso e verde nel registro di origine usando la matrice di mapping dell'ambiente di urto 2D. Il risultato viene aggiunto al set di coordinate della trama corrispondente al numero di registro di destinazione. Una correzione della luminanza viene applicata usando il valore di luminance e i valori della fase della trama di distorsione. Il risultato viene usato per campionare la fase di trama corrente.

Può essere usato per un'ampia gamma di tecniche basate sulla perturbazione degli indirizzi, ad esempio il mapping dell'ambiente falso per pixel.

Questa operazione interpreta sempre du e dv come quantità firmate. Per le versioni 1 0 e 1 1, il modificatore di \_ input Source Register Signed \_ [Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ bx2) non è consentito nell'argomento di input.

Questa istruzione produce risultati definiti quando le trame di input contengono dati in formato misto. Per altre informazioni sui formati di superficie, vedere [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



Questo esempio illustra i calcoli evasi all'interno dell'istruzione .


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



u' = TextureCoordinates(stage m)<sub>u</sub> +

D3DTSS \_ BUMPENVMAT00(stage m) \* t(n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT10(stage m) \* t(n)<sub>G</sub>

v' = TextureCoordinates(stage m)<sub>v</sub> +

D3DTSS \_ BUMPENVMAT01(stage m) \* t(n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT11(stage m) \* t(n)<sub>G</sub>

t(m)<sub>RGBA</sub> = TextureSample(stage m) usando (u',v') come coordinate

t(m)<sub>RGBA</sub> = t(m)<sub>RGBA</sub>\*

\[(t(n)<sub>B</sub> \* D3DTSS \_ BUMPENVLSCALE(stage m)) +

D3DTSS \_ BUMPENVLOFFSET(stage m)\]

I dati di registrazione letti da un'istruzione [texbem](texbem---ps.md) o texbeml non possono essere letti in un secondo momento, ad eccezione di un altro texbem o texbeml.


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

Ecco un esempio di shader con le mappe di trama identificate e le fasi della trama identificate.


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



Questo esempio richiede le trame seguenti nelle fasi di trama seguenti.

-   Alla fase 0 viene assegnata una mappa di rilievo con dati di perturbazione (du, dv).
-   Alla fase 1 viene assegnata una mappa trama con dati di colore.
-   texbeml imposta i dati della matrice nella fase di trama campionata. Questo è diverso dalla funzionalità della pipeline di funzioni fisse in cui i dati di perturbazione e le matrici occupano la stessa fase di trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 