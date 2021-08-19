---
title: Metodo GETBackingStore ID3DX11EffectDepthStencilVariable (D3dx11effect.h)
description: Ottiene un puntatore a una variabile che contiene lo stato depth-stencil.
ms.assetid: 6aeed5ac-f0ee-4e8c-b87b-022f58c9094c
keywords:
- Metodo GetBackingStore Direct3D 11
- Metodo GetBackingStore Interfaccia Direct3D 11, ID3DX11EffectDepthStencilVariable
- ID3DX11EffectDepthStencilVariable interface Direct3D 11 , Metodo GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe2387b6cc071e9146176e6cf8b84da1870c0671572f184fea7e6cbadef03d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989841"
---
# <a name="id3dx11effectdepthstencilvariablegetbackingstore-method"></a>Metodo ID3DX11EffectDepthStencilVariable::GetBackingStore

Ottiene un puntatore a una variabile che contiene lo stato depth-stencil.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBackingStore(
   UINT                     Index,
   D3D11_DEPTH_STENCIL_DESC *pDepthStencilDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indicizzare in una matrice di descrizioni dello stato depth-stencil. Se nell'effetto è presente una sola variabile depth-stencil, usare 0.

</dd> <dt>

*pDepthStencilDesc* 
</dt> <dd>

Tipo: **[ **D3D11 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)\***

Puntatore a una descrizione depth-stencil-state (vedere [**D3D11 \_ DEPTH \_ STENCIL \_ DESC).**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Le variabili di effetto vengono salvate in memoria nell'archivio di backup. Quando viene applicata una tecnica, i valori nell'archivio di backup vengono copiati nel dispositivo. I dati dell'archivio di backup possono essere usati per ricreare la variabile quando necessario.

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectDepthStencilVariable](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

