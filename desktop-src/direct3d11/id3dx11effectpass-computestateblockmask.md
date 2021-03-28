---
title: Metodo ID3DX11EffectPass ComputeStateBlockMask (D3dx11effect. h)
description: Genera una maschera per consentire o impedire le modifiche di stato.
ms.assetid: 584be931-0e22-43e6-b852-f0d2ab050bdd
keywords:
- Metodo ComputeStateBlockMask Direct3D 11
- Metodo ComputeStateBlockMask Direct3D 11, interfaccia ID3DX11EffectPass
- Interfaccia ID3DX11EffectPass Direct3D 11, metodo ComputeStateBlockMask
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
ms.openlocfilehash: b8fc5cb32ce9e9644d7d5b62868bfa99f150cc94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982364"
---
# <a name="id3dx11effectpasscomputestateblockmask-method"></a>Metodo ID3DX11EffectPass:: ComputeStateBlockMask

Genera una maschera per consentire o impedire le modifiche di stato.

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

Tipo: **[ **D3DX11 \_ state \_ Block \_ mask**](d3dx11-state-block-mask.md)\***

Puntatore a una maschera a blocchi di stato (vedere [**D3DX11 \_ state \_ Block \_ mask**](d3dx11-state-block-mask.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





