---
title: texld - ps_1_4
description: Carica il registro di destinazione con i dati di colore (RGBA) campionati usando il contenuto del registro di origine come coordinate della trama. La trama campionata è la trama associata al numero di registro di destinazione.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc940379c8910b45d3dcb476054cf4362a6a96bc2c5df784c8ed5ca815a093fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505810"
---
# <a name="texld---ps_1_4"></a>texld - ps \_ 1 \_ 4

Carica il registro di destinazione con i dati di colore (RGBA) campionati usando il contenuto del registro di origine come coordinate della trama. La trama campionata è la trama associata al numero di registro di destinazione.



| texld dst, src |
|----------------|



 

## <a name="registers"></a>Registri



| Valore         | Descrizione                     | Vn        | Cn  | Tn  | Rn  | Versione pixel shader              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| Dst      | Registro di destinazione |           |     |     | x   | 1\_4         |
| src      | Registro di origine      |           |     | x   |     | 1 \_ 4 fase 1 |
|          |                      |           |     | x   | x   | 1 \_ 4 fase   |



 

Quando si usa r(n) come registro di origine, i primi tre componenti (XYZ) devono essere stati inizializzati nella fase precedente dello shader.

Per altre informazioni sui registri, vedere [ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Commenti

Questa istruzione campio la trama nella fase della trama associata al numero di registro di destinazione. La trama viene campionata usando i dati delle coordinate della trama del registro di origine.

La sintassi per le istruzioni texld e texcrd espone il supporto per una divisione proiettata con un modificatore di registro texture. Per pixel shader versione 1.4, il flag di trasformazione della trama D3DTTFF \_ PROJECTED viene sempre ignorato.

Regole per l'uso di texld:

1.  Lo stesso modificatore .xyz o .xyw deve essere applicato a ogni lettura di un singolo registro t(n) all'interno di entrambe le istruzioni texcrd o texld. Se .xyw viene usato nelle operazioni di lettura del registro t(n), questo può essere misto con altre operazioni di lettura dello stesso registro t(n) usando .xyw \_ dw.
2.  Il modificatore dz source è valido solo in texld con il registro di origine \_ r(n) (solo fase 2).
3.  Il \_ modificatore dz source può essere usato non più di due volte per ogni shader.



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texld                 |      |      |      | x    |      |      |       |      |       |



 

## <a name="examples"></a>Esempio

L'istruzione texld offre un certo controllo sui componenti dei dati delle coordinate della trama di origine da usare. Il set completo di sintassi consentita per texld segue e include tutti i modificatori del registro di origine validi, i selettori e le combinazioni di maschera di scrittura.


```
texld  r(m), t(n).xyz
// Uses xyz from t(n) to sample 1D, 2D, or 3D texture
```




```
texld  r(m), t(n)
// Same as previous
```




```
texld  r(m), t(n).xyw
// Uses xyw (skipping z) from t(n) to sample 1D, 2D or 3D texture
```




```
texld  r(m), t(n)_dw.xyw  
// Samples 1D or 2D texture at x/w, y/w from t(n). The result
// is undefined for a cube-map lookup.
```




```
texld  r(m), r(n).xyz
// Samples 1D, 2D, or 3D texture at xyz from r(m) 
// This is possible in the second phase of the shader
```




```
texld  r(m), r(n)
// Same as previous
```




```
texld  r(m), r(n)_dz.xyz
// Samples 1D or 2D texture at x/z, y/z from r(m)
// Possible only in second phase
// The result is undefined for a cube-map lookup
```




```
texld  r(n), r(n)_dz
// Same as previous
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




