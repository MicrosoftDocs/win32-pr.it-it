---
title: Metodo ID3DX11EffectDepthStencilVariable GetBackingStore (D3dx11effect. h)
description: Ottenere un puntatore a una variabile che contiene lo stato di stencil Depth.
ms.assetid: 6aeed5ac-f0ee-4e8c-b87b-022f58c9094c
keywords:
- Metodo GetBackingStore Direct3D 11
- Metodo GetBackingStore Direct3D 11, interfaccia ID3DX11EffectDepthStencilVariable
- Interfaccia ID3DX11EffectDepthStencilVariable Direct3D 11, metodo GetBackingStore
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
ms.openlocfilehash: 9335817b9c954958c97294a88291f83bf0e967d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982307"
---
# <a name="id3dx11effectdepthstencilvariablegetbackingstore-method"></a>Metodo ID3DX11EffectDepthStencilVariable:: GetBackingStore

Ottenere un puntatore a una variabile che contiene lo stato di stencil Depth.

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indicizzare in una matrice di descrizioni dello stato di depth-stencil. Se è presente una sola variabile di stencil Depth nell'effetto, usare 0.

</dd> <dt>

*pDepthStencilDesc* 
</dt> <dd>

Tipo: **[ **d3d11 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)\***

Puntatore a una descrizione dello stato di depth-stencil (vedere [**d3d11 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Le variabili di effetto vengono salvate in memoria nell'archivio di backup; Quando viene applicata una tecnica, i valori nell'archivio di backup vengono copiati nel dispositivo. Quando necessario, è possibile utilizzare i dati dell'archivio di backup per ricreare la variabile.

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectDepthStencilVariable](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

