---
title: Metodo ID3DX11EffectSamplerVariable UndoSetSampler (D3dx11effect.h)
description: Ripristinare uno stato del campionatore impostato in precedenza.
ms.assetid: bb837b12-d6c3-47e9-a0a1-0bfcfe0f3e4e
keywords:
- Metodo UndoSetSampler Direct3D 11
- Metodo UndoSetSampler Direct3D 11, interfaccia ID3DX11EffectSamplerVariable
- ID3DX11EffectSamplerVariable interface Direct3D 11 , UndoSetSampler method
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.UndoSetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833bc7cd9ca867e1fe788c339b37c682a4167e36222ce1222a2c9afdb6934bcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791891"
---
# <a name="id3dx11effectsamplervariableundosetsampler-method"></a>Metodo ID3DX11EffectSamplerVariable::UndoSetSampler

Ripristinare uno stato del campionatore impostato in precedenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UndoSetSampler(
   UINT Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indicizzare in una matrice di interfacce del campionatore. Se è presente una sola interfaccia del campionatore, usare 0.

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

 

