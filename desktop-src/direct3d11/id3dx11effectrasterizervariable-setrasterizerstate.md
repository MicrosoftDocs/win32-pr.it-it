---
title: Metodo ID3DX11EffectRasterizerVariable SetRasterizerState (D3dx11effect.h)
description: Imposta lo stato di rasterizzazione.
ms.assetid: b2cd93fb-77bb-4a39-b686-7b8f683c9172
keywords:
- Metodo SetRasterizerState Direct3D 11
- Metodo SetRasterizerState Direct3D 11, interfaccia ID3DX11EffectRasterizerVariable
- ID3DX11EffectRasterizerVariable interface Direct3D 11 , SetRasterizerState method
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.SetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da95b99a3707b9fd9d05e9343e36a095cf3d6a346180df69ad6ecd3f749febd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534329"
---
# <a name="id3dx11effectrasterizervariablesetrasterizerstate-method"></a>Metodo ID3DX11EffectRasterizerVariable::SetRasterizerState

Imposta lo stato di rasterizzazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState *pRasterizerState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice in una matrice di interfacce di rasterizzazione. Se è presente una sola interfaccia di rasterizzazione, usare 0.

</dd> <dt>

*pRasterizerState* 
</dt> <dd>

Tipo: **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\***

Puntatore a [**un'interfaccia ID3D11RasterizerState.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)

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

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

