---
title: tex2Dlod
description: Campione una trama 2D con mipmap. Il LOD mipmap è specificato in t.w.
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- tex2Dlod HLSL
topic_type:
- apiref
api_name:
- tex2Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9581418eb2a3d8736fcd0e125eaafec11494e6b6d5471cef33f9592475d5ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725679"
---
# <a name="tex2dlod"></a>tex2Dlod

Campione una trama 2D con mipmap. Il LOD mipmap è specificato in t.w.



| ret tex2Dlod(s, t) |
|--------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/> | \[nello \] stato del campionatore.<br/>      |
| <span id="t"></span><span id="T"></span>*T*<br/> | \[in \] Coordinata trama.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore dei dati della trama.

## <a name="type-description"></a>Descrizione del tipo



| Nome | Ingresso/Uscita | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Oggetto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| Ret  | in uscita    | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) e modelli shader superiori | sì       |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md)                          | no        |



 

## <a name="remarks"></a>Commenti

A partire da Direct3D 10, è possibile usare la nuova sintassi HLSL per accedere alle trame e ad altre risorse. È possibile sostituire funzioni di ricerca trame di tipo intrinseco, ad esempio **tex2Dlod**, con uno stile più orientato agli oggetti. In questo stile orientato a oggetti le trame sono disaccoccodate dai campionatori e dispongono di metodi per il caricamento e il campionamento.

Per campionare una trama 2D, invece di **usare tex2Dlod** come in questo codice:


```
sampler S;
...
color = tex2Dlod(S, Location);
```



Usare il [metodo SampleLevel](dx-graphics-hlsl-to-samplelevel.md) di un [**oggetto Texture**](dx-graphics-hlsl-to-type.md) come nel codice seguente:


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



Per usare le funzioni di ricerca di trame di tipo intrinseco, ad esempio **tex2Dlod**, con il modello [shader 4](dx-graphics-hlsl-sm4.md) e versioni successive, usare [**D3DCOMPILE \_ ENABLE \_ BACKWARDS \_ COMPATIBILITY**](d3dcompile-constants.md) per la compilazione. Tuttavia, se si vuole usare come destinazione il modello shader 4 e versioni successive (anche [ \* \_ 4 \_ 0 \_ livello \_ 9) \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)con il codice di stile orientato agli oggetti più recente, eseguire la migrazione alla sintassi HLSL più recente.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

