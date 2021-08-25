---
title: Metodo ID3DX11EffectTechnique ComputeStateBlockMask (D3dx11effect.h)
description: Calcolare una maschera di blocco di stato per consentire o impedire modifiche dello stato.
ms.assetid: 4fd6061d-6ca5-4e3f-b031-fae98f3de057
keywords:
- Metodo ComputeStateBlockMask Direct3D 11
- Metodo ComputeStateBlockMask Direct3D 11, interfaccia ID3DX11EffectTechnique
- ID3DX11EffectTechnique interface Direct3D 11 , ComputeStateBlockMask method
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf7a221cd685eb31b068ae6144514adb70ffa42c654d9e1a3249db5302e0aa6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894761"
---
# <a name="id3dx11effecttechniquecomputestateblockmask-method"></a>Metodo ID3DX11EffectTechnique::ComputeStateBlockMask

Calcolare una maschera di blocco di stato per consentire o impedire modifiche dello stato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStateBlockMask* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ STATE \_ BLOCK \_ MASK**](d3dx11-state-block-mask.md)\***

Puntatore a una maschera di blocco di stato (vedere [**D3DX11 \_ STATE \_ BLOCK \_ MASK).**](d3dx11-state-block-mask.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

 





