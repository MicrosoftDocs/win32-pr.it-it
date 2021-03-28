---
title: Metodo ID3DX11EffectDepthStencilViewVariable GetDepthStencilArray (D3dx11effect. h)
description: Ottenere una matrice di risorse di visualizzazione degli stencil di profondità.
ms.assetid: 92b2d9b1-6cf8-4523-88e0-bcd09b95477c
keywords:
- Metodo GetDepthStencilArray Direct3D 11
- Metodo GetDepthStencilArray Direct3D 11, interfaccia ID3DX11EffectDepthStencilViewVariable
- Interfaccia ID3DX11EffectDepthStencilViewVariable Direct3D 11, metodo GetDepthStencilArray
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
ms.openlocfilehash: d7b7b886049413be542108257a47a3b1e3899910
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982445"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencilarray-method"></a>Metodo ID3DX11EffectDepthStencilViewVariable:: GetDepthStencilArray

Ottenere una matrice di risorse di visualizzazione degli stencil di profondità.

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

Puntatore a una matrice di interfacce di visualizzazione stencil profondità. Vedere [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).

</dd> <dt>

*Offset* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indice della matrice in base zero per ottenere la prima interfaccia.

</dd> <dt>

*Count* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Numero di elementi nella matrice.

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

[ID3DX11EffectDepthStencilViewVariable](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

