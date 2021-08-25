---
title: Metodo ID3DX11EffectDepthStencilViewVariable GetDepthStencilArray (D3dx11effect.h)
description: Ottiene una matrice di risorse depth-stencil-view.
ms.assetid: 92b2d9b1-6cf8-4523-88e0-bcd09b95477c
keywords:
- Metodo GetDepthStencilArray Direct3D 11
- Metodo GetDepthStencilArray Interfaccia Direct3D 11, ID3DX11EffectDepthStencilViewVariable
- ID3DX11EffectDepthStencilViewVariable interface Direct3D 11 , GetDepthStencilArray method
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencilArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2981d3da9bd66066009f2b7e9826514f34681935d0b49fe1b014ea9f847beea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952881"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencilarray-method"></a>Metodo ID3DX11EffectDepthStencilViewVariable::GetDepthStencilArray

Ottiene una matrice di risorse depth-stencil-view.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDepthStencilArray(
   ID3D11DepthStencilView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppResources* 
</dt> <dd>

Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***

Puntatore a una matrice di interfacce depth-stencil-view. Vedere [**ID3D11DepthStencilView.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)

</dd> <dt>

*Offset* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice di matrice in base zero per ottenere la prima interfaccia.

</dd> <dt>

*Count* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Numero di elementi nella matrice.

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

[ID3DX11EffectDepthStencilViewVariable](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

