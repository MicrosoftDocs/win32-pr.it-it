---
title: Metodo ID3DX11EffectBlendVariable UndoSetBlendState (D3dx11effect. h)
description: Ripristina uno stato di Blend impostato in precedenza.
ms.assetid: 375c225b-558f-4ad0-81e7-62eff3e28cf1
keywords:
- Metodo UndoSetBlendState Direct3D 11
- Metodo UndoSetBlendState Direct3D 11, interfaccia ID3DX11EffectBlendVariable
- Interfaccia ID3DX11EffectBlendVariable Direct3D 11, metodo UndoSetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.UndoSetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e117eafa9b6379b2240cf491809c58d8600d840f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996077"
---
# <a name="id3dx11effectblendvariableundosetblendstate-method"></a>Metodo ID3DX11EffectBlendVariable:: UndoSetBlendState

Ripristina uno stato di Blend impostato in precedenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UndoSetBlendState(
   UINT Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indicizzare in una matrice di interfacce di stato di Blend. Se è presente una sola interfaccia di stato di Blend, usare 0.

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

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

