---
title: tex2Dlod
description: Campiona una trama 2D con mipmap. Il mipmap LOD è specificato in t.w.
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- HLSL tex2Dlod
topic_type:
- apiref
api_name:
- tex2Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f63a922fe86dc10d984369a1a872f84089b4db34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976647"
---
# <a name="tex2dlod"></a>tex2Dlod

Campiona una trama 2D con mipmap. Il mipmap LOD è specificato in t.w.



| tex2Dlod RET (s, t) |
|--------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/> | \[nello \] stato del campionatore.<br/>      |
| <span id="t"></span><span id="T"></span>*t*<br/> | \[nella \] coordinata di trama.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore dei dati della trama.

## <a name="type-description"></a>Descrizione del tipo



| Nome | Ingresso/Uscita | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in ingresso     | [**oggetto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| u    | in ingresso     | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| RET  | in uscita    | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) e modelli shader più elevati | sì       |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | no        |



 

## <a name="remarks"></a>Commenti

A partire da Direct3D 10, è possibile usare la nuova sintassi HLSL per accedere alle trame e ad altre risorse. È possibile sostituire le funzioni di ricerca di trama di tipo intrinseco, ad esempio **tex2Dlod**, con uno stile più orientato agli oggetti. In questo stile orientato a oggetti, le trame vengono disaccoppiate dai sampler e dispongono di metodi per il caricamento e il campionamento.

Per campionare una trama 2D, invece di usare **tex2Dlod** come nel codice seguente:


```
sampler S;
...
color = tex2Dlod(S, Location);
```



Usare il metodo [SampleLevel](dx-graphics-hlsl-to-samplelevel.md) di un [**oggetto texture**](dx-graphics-hlsl-to-type.md) come nel codice seguente:


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



Per utilizzare le funzioni di ricerca di trama di tipo intrinseco, ad esempio **tex2Dlod**, con [Shader Model 4](dx-graphics-hlsl-sm4.md) e versioni successive, utilizzare D3DCOMPILE per consentire la compilazione con la [**\_ \_ \_ compatibilità**](d3dcompile-constants.md) con le versioni precedenti. Tuttavia, se si desidera destinare il modello Shader 4 e versioni successive (anche [ \* \_ 4 \_ 0 \_ livello \_ 9 \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) con il codice di stile orientato a oggetti più recente, eseguire la migrazione alla sintassi HLSL più recente.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

