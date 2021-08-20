---
title: Metodo ID3DX11EffectBlendVariable GetBlendState (D3dx11effect.h)
description: Ottenere un puntatore a un'interfaccia dello stato di blend.
ms.assetid: ab4ee765-b5ad-4dc3-9b00-48052528d3bd
keywords:
- Metodo GetBlendState Direct3D 11
- Metodo GetBlendState Direct3D 11, interfaccia ID3DX11EffectBlendVariable
- ID3DX11EffectBlendVariable interface Direct3D 11 , GetBlendState method
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 925e6df2571806f71d5d324f825d53fab3bc481ec80c872954ebf18e89c223a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099034"
---
# <a name="id3dx11effectblendvariablegetblendstate-method"></a>Metodo ID3DX11EffectBlendVariable::GetBlendState

Ottenere un puntatore a un'interfaccia dello stato di blend.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBlendState(
   UINT             Index,
   ID3D11BlendState **ppBlendState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indicizzare in una matrice di interfacce dello stato di blend. Se è presente una sola interfaccia dello stato di blend, usare 0.

</dd> <dt>

*ppBlendState* 
</dt> <dd>

Tipo: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\*\***

Indirizzo di un puntatore a un'interfaccia dello stato di blend (vedere [**ID3D11BlendState).**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)

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

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

