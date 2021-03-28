---
title: texbem-PS
description: Applicare una trasformazione della mappa dell'ambiente di Bump Fake. Questa operazione viene eseguita modificando i dati dell'indirizzo di trama del registro di destinazione, usando i dati di risoluzione dell'indirizzo (du, DV) e una matrice di ambiente urto 2D.
ms.assetid: 8e773f4a-c7a2-4caf-973f-8f50dccc9c04
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f026819b268836fd7d4c1d550033ceefdf0bbbf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976695"
---
# <a name="texbem---ps"></a>texbem-PS

Applicare una trasformazione della mappa dell'ambiente di Bump Fake. Questa operazione viene eseguita modificando i dati dell'indirizzo di trama del registro di destinazione, usando i dati di risoluzione dell'indirizzo (du, DV) e una matrice di ambiente urto 2D.

## <a name="syntax"></a>Sintassi



| texbem DST, src |
|-----------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texbem                | x    | x    | x    |      |      |      |       |      |       |



 

I dati di colore rosso e verde nel registro src vengono interpretati come dati di perturbazione (du, DV).

Questa istruzione trasforma i componenti rossi e verdi nel registro di origine usando la matrice di mapping dell'ambiente Bump 2D. Il risultato viene aggiunto al set di coordinate di trama corrispondente al numero di registro di destinazione e viene usato per campionare la fase di trama corrente.

Questa operazione interpreta sempre du e DV come quantità con segno. Per le versioni 1 \_ 0 e 1 \_ 1, il modificatore di input con [segno di ridimensionamento del registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) non è consentito nell'argomento di input.

Questa istruzione genera risultati definiti quando le trame di input contengono dati in formato firmato. I dati in formato misto funzionano solo se i primi due canali contengono dati firmati. Per ulteriori informazioni sui formati di superficie, vedere [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

Questo può essere usato per diverse tecniche in base alla turbativa degli indirizzi, tra cui il mapping dell'ambiente per pixel Fake e l'illuminazione diffusa (bump mapping).

Quando si utilizza questa istruzione, i registri di trama devono seguire la sequenza seguente.


```
// The texture assigned to stage t(n) contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbem  t(m),  t(n)      where m > n
```



I calcoli eseguiti nell'istruzione sono riportati di seguito.


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
```



u ' = TextureCoordinates (fase m)<sub>u</sub> + D3DTSS \_ BUMPENVMAT00 (fase m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT10 (fase m) \* t (n)<sub>g</sub> v'= TextureCoordinates (fase m)<sub>v</sub> + D3DTSS \_ BUMPENVMAT01 (fase m) \* t (n)<sub>r</sub> + D3DTSS \_ BUMPENVMAT11 (fase m) \* t (n)<sub>g</sub> t (m)<sub>RGBA</sub> = TextureSample (fase m)

uso di (u ', v') come coordinate

Registrare i dati letti da un'istruzione texbem-PS o [texbeml-PS](texbeml---ps.md) non possono essere letti in un secondo momento, ad eccezione di un altro texbem-PS o texbeml-PS.


```
// This example demonstrates the validation error caused by t0 being reread:
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
texbem t1, t0       ; Compute (u',v')
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



texbem richiede le seguenti trame nelle fasi di trama seguenti.

-   Alla fase 0 viene assegnata una mappa Bump con i dati di perturbazione (du, DV).
-   La fase 1 USA una mappa di trama con dati di colore.
-   Questa istruzione imposta i dati della matrice nella fase di trama campionata.
-   Si tratta di una differenza rispetto alla funzionalità della pipeline della funzione fissa in cui i dati di perturbazione e le matrici occupano la stessa fase della trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 