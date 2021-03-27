---
title: Metodo ID3DX11EffectRasterizerVariable GetBackingStore (D3dx11effect. h)
description: Ottiene un puntatore a una variabile che contiene lo stato rasteriser.
ms.assetid: aff62a6c-bdef-49ad-9492-5db0878f632e
keywords:
- Metodo GetBackingStore Direct3D 11
- Metodo GetBackingStore Direct3D 11, interfaccia ID3DX11EffectRasterizerVariable
- Interfaccia ID3DX11EffectRasterizerVariable Direct3D 11, metodo GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1941ba93b69f1d07eeebaa6c1f0c9323f5c0a49e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058664"
---
# <a name="id3dx11effectrasterizervariablegetbackingstore-method"></a>Metodo ID3DX11EffectRasterizerVariable:: GetBackingStore

Ottiene un puntatore a una variabile che contiene lo stato rasteriser.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBackingStore(
   UINT                  Index,
   D3D11_RASTERIZER_DESC *pRasterizerDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indicizzare in una matrice di descrizioni dello stato rasteriser. Se è presente una sola variabile rasteriser nell'effetto, usare 0.

</dd> <dt>

*pRasterizerDesc* 
</dt> <dd>

Tipo: **[ **d3d11 \_ rasterizzator \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***

Un puntatore a una descrizione dello stato rasteriser (vedere la pagina relativa al [**\_ rasterizzatore d3d11 \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)).

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

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

