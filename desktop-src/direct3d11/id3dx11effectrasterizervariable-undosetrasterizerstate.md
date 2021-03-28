---
title: Metodo ID3DX11EffectRasterizerVariable UndoSetRasterizerState (D3dx11effect. h)
description: Ripristina uno stato di rasterizzazione impostato in precedenza.
ms.assetid: 2801479c-cb70-4950-9888-73e271b669aa
keywords:
- Metodo UndoSetRasterizerState Direct3D 11
- Metodo UndoSetRasterizerState Direct3D 11, interfaccia ID3DX11EffectRasterizerVariable
- Interfaccia ID3DX11EffectRasterizerVariable Direct3D 11, metodo UndoSetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.UndoSetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed05aa7380a1fb08bbd12d36328d33fa64fb7500
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235219"
---
# <a name="id3dx11effectrasterizervariableundosetrasterizerstate-method"></a>Metodo ID3DX11EffectRasterizerVariable:: UndoSetRasterizerState

Ripristina uno stato di rasterizzazione impostato in precedenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UndoSetRasterizerState(
   UINT Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indicizzare in una matrice di interfacce di rasterizzazione. Se è presente una sola interfaccia di rasterizzazione, usare 0.

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

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

