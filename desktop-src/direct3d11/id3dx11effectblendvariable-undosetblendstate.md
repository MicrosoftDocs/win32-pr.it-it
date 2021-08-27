---
title: Metodo ID3DX11EffectBlendVariable UndoSetBlendState (D3dx11effect.h)
description: Ripristina uno stato di blend impostato in precedenza.
ms.assetid: 375c225b-558f-4ad0-81e7-62eff3e28cf1
keywords:
- Metodo UndoSetBlendState Direct3D 11
- Metodo UndoSetBlendState Direct3D 11, interfaccia ID3DX11EffectBlendVariable
- Id3DX11EffectBlendVariable interface Direct3D 11 , UndoSetBlendState method
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
ms.openlocfilehash: 5fefb1e59ef3ef30bcd21700a2573830e3178f574fe631ab4c7373b0bddd5fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046479"
---
# <a name="id3dx11effectblendvariableundosetblendstate-method"></a>Metodo ID3DX11EffectBlendVariable::UndoSetBlendState

Ripristina uno stato di blend impostato in precedenza.

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

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indicizzare in una matrice di interfacce di stato di blend. Se è presente una sola interfaccia dello stato di blend, usare 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

