---
title: Metodo ID3DX11EffectPass ComputeStateBlockMask (D3dx11effect.h)
description: Generare una maschera per consentire o impedire modifiche dello stato.
ms.assetid: 584be931-0e22-43e6-b852-f0d2ab050bdd
keywords:
- Metodo ComputeStateBlockMask Direct3D 11
- Metodo ComputeStateBlockMask Direct3D 11, interfaccia ID3DX11EffectPass
- ID3DX11EffectPass interface Direct3D 11 , ComputeStateBlockMask method
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17198c076d200631142207189059ada425e9ec1ddf6e3c8a8d40499e40aa21a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535057"
---
# <a name="id3dx11effectpasscomputestateblockmask-method"></a>Metodo ID3DX11EffectPass::ComputeStateBlockMask

Generare una maschera per consentire o impedire modifiche dello stato.

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





