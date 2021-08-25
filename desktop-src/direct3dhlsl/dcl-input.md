---
title: dcl_input (sm4 - asm)
description: Input dcl \_ (sm4 - asm)
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8214287a4afb4c683a94e213cdfed133c03219e2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467008"
---
# <a name="dcl_input-sm4---asm"></a>Input dcl \_ (sm4 - asm)

Dichiara un registro di input shader.



| dcl \_ input v N *\[ .mask , \] \[ interpolationMode \]* |
|-------------------------------------------------|



 




| Elemento | Descrizione | 
|------|-------------|
| <span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em><br /> | [in] Registro dei dati dei vertici. <br /><ul><li><em>N</em> è un numero intero che identifica il numero di registro.</li><li><em>[.mask]</em> è una maschera componente facoltativa (.xyzw) che specifica quali componenti del registro usare.</li></ul> | 
| <span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em><br /> | [in] Facoltativo. La modalità di interpolazione, che viene rispettata solo nei pixel shader di input. Può essere uno dei valori seguenti: <br /><ul><li>constant: non interpolare tra valori di registro.</li><li>linear: interpolazione lineare tra valori di registro.</li><li>linearCentroid: uguale a lineare ma con chiusura al centro durante il multicampionamento.</li><li>linearNoperspective: uguale a lineare ma senza correzione prospettica.</li><li>linearNoperspectiveCentroid: uguale a lineare, con chiusura centroide in caso di multicampionamento, senza correzione della prospettiva.</li></ul> | 




 

### <a name="interpolation-notes"></a>Note sull'interpolazione

Per impostazione predefinita, gli attributi dei vertici vengono interpolati da un centro pixel quando si esegue l'anti-aliasing multicampionamento. Se un centro pixel non è coperto, un attributo viene estrapolato in un centro pixel prima dell'interpolazione.

Per un pixel non completamente coperto o un attributo che non copre un centro pixel, è possibile specificare il campionamento centroide che forza il campionamento in un punto qualsiasi all'interno dell'area coperta del pixel. Poiché viene applicata una maschera di esempio (se usata) prima del calcolo del centroide, non è possibile scegliere come posizione centrale qualsiasi posizione del campione mascherata dalla maschera di esempio.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Per identificare l'input come valore di sistema, usare [dcl \_ input \_ sv (sm4 - asm).](dcl-input-sv.md)

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. Non è possibile creare uno shader in linguaggio assembly usando il modello shader 4.

## <a name="example"></a>Esempio

Di seguito sono riportati alcuni esempi.


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
```



## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





