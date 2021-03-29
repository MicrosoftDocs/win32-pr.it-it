---
title: texld-ps_1_4
description: Carica il registro di destinazione con i dati di colore (RGBA) campionati utilizzando il contenuto del registro di origine come coordinate di trama. La trama campionata è la trama associata al numero di registro di destinazione.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 23827dffc396a40be134be4db3996d2e9f498288
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993144"
---
# <a name="texld---ps_1_4"></a>texld-PS \_ 1 \_ 4

Carica il registro di destinazione con i dati di colore (RGBA) campionati utilizzando il contenuto del registro di origine come coordinate di trama. La trama campionata è la trama associata al numero di registro di destinazione.



| texld DST, src |
|----------------|



 

## <a name="registers"></a>Registri



| Argomento | Descrizione          | Registri |     |     |     | Versione      |
|----------|----------------------|-----------|-----|-----|-----|--------------|
|          |                      | VN        | CN  | TN  | RN  |              |
| DST      | Registro destinazione |           |     |     | x   | 1\_4         |
| src      | Registro di origine      |           |     | x   |     | 1 \_ 4 fase 1 |
|          |                      |           |     | x   | x   | 1 \_ fase 4   |



 

Quando si usa r (n) come registro di origine, è necessario inizializzare i primi tre componenti (XYZ) nella fase precedente dello shader.

Per ulteriori informazioni sui registri, vedere la pagina relativa ai registri PS 1 [ \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS 1 \_ \_ 3 \_ \_ PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Commenti

Questa istruzione esegue il campionamento della trama nella fase della trama associata al numero di registro di destinazione. La trama viene campionata usando i dati delle coordinate di trama del registro di origine.

La sintassi per le istruzioni texld e texcrd espone il supporto per una divisione proiettiva con un modificatore di registro di trama. Per pixel shader versione 1,4, il \_ flag di trasformazione trama D3DTTFF proiettato viene sempre ignorato.

Regole per l'uso di texld:

1.  Lo stesso modificatore. xyz o. XYW deve essere applicato a ogni lettura di un singolo registro t (n) nelle istruzioni texcrd o texld. Se viene usato. XYW nelle letture del registro t (n), questo può essere misto con altre letture dello stesso registro t (n) con. XYW \_ DW.
2.  Il \_ modificatore di origine DZ è valido solo in texld con il registro di origine r (n) (solo in questo caso la fase 2).
3.  Il \_ modificatore di origine DZ può essere usato non più di due volte per shader.



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texld                 |      |      |      | x    |      |      |       |      |       |



 

## <a name="examples"></a>Esempio

L'istruzione texld offre un certo controllo sui componenti utilizzati per i dati delle coordinate di trama di origine. Segue il set completo di sintassi consentita per texld e include tutti i modificatori del registro di origine, i selettori e le combinazioni di maschere di scrittura validi.


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

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




