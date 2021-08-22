---
title: Metodo GetSampler ID3DX11EffectSamplerVariable (D3dx11effect.h)
description: Ottenere un puntatore a un'interfaccia del campionatore.
ms.assetid: ac2a05f1-e3ca-4ebf-b655-34133c4e50ac
keywords:
- Metodo GetSampler Direct3D 11
- Metodo GetSampler Direct3D 11, interfaccia ID3DX11EffectSamplerVariable
- ID3DX11EffectSamplerVariable interface Direct3D 11 , GetSampler method
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc9c400f3596d380f5e671eaa04f4e4340bde385230f331e3e2fdc7ee1a92f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045829"
---
# <a name="id3dx11effectsamplervariablegetsampler-method"></a>Metodo ID3DX11EffectSamplerVariable::GetSampler

Ottenere un puntatore a un'interfaccia del campionatore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSampler(
   UINT               Index,
   ID3D11SamplerState **ppSampler
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indicizzare in una matrice di interfacce del campionatore. Se è presente una sola interfaccia del campionatore, usare 0.

</dd> <dt>

*ppSampler* 
</dt> <dd>

Tipo: **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\*\***

Indirizzo di un puntatore a un'interfaccia del campionatore (vedere [**ID3D11SamplerState).**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)

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

[ID3DX11EffectSamplerVariable](id3dx11effectsamplervariable.md)
</dt> </dl>

 

