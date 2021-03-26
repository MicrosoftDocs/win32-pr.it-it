---
title: Metodo ID3DX11EffectSamplerVariable GetBackingStore (D3dx11effect. h)
description: Ottiene un puntatore a una variabile che contiene lo stato del campionatore.
ms.assetid: b188fb86-f54b-481e-9110-7b8af70ff303
keywords:
- Metodo GetBackingStore Direct3D 11
- Metodo GetBackingStore Direct3D 11, interfaccia ID3DX11EffectSamplerVariable
- Interfaccia ID3DX11EffectSamplerVariable Direct3D 11, metodo GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03f2d6ac3035d1dd2fd3aee8950135d7b4481862
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355364"
---
# <a name="id3dx11effectsamplervariablegetbackingstore-method"></a>Metodo ID3DX11EffectSamplerVariable:: GetBackingStore

Ottiene un puntatore a una variabile che contiene lo stato del campionatore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBackingStore(
   UINT               Index,
   D3D11_SAMPLER_DESC *pSamplerDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indicizzare in una matrice di descrizioni del campionatore. Se è presente una sola variabile del campionatore nell'effetto, usare 0.

</dd> <dt>

*pSamplerDesc* 
</dt> <dd>

Tipo: **[ **d3d11 \_ Sampler \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***

Puntatore a una descrizione del campionatore (vedere [**d3d11 \_ Sampler \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)).

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

[ID3DX11EffectSamplerVariable](id3dx11effectsamplervariable.md)
</dt> </dl>

 

