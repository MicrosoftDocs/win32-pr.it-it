---
title: Metodo ID3DX11EffectUnorderedAccessViewVariable SetUnorderedAccessView (D3dx11effect.h)
description: Impostare un oggetto unordered-access-view.
ms.assetid: a147879c-c5cf-4453-b27f-8716cb33962b
keywords:
- Metodo SetUnorderedAccessView Direct3D 11
- Metodo SetUnorderedAccessView Direct3D 11, ID3DX11EffectUnorderedAccessViewVariable
- ID3DX11EffectUnorderedAccessViewVariable interface Direct3D 11, SetUnorderedAccessView method
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.SetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d95dc15b0b79475cf7b8a731df291c73cb193db44fdc5bb917606dd916d6757
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565741"
---
# <a name="id3dx11effectunorderedaccessviewvariablesetunorderedaccessview-method"></a>Metodo ID3DX11EffectUnorderedAccessViewVariable::SetUnorderedAccessView

Impostare un oggetto unordered-access-view.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetUnorderedAccessView(
   ID3D11UnorderedAccessView *pResource
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pResource* 
</dt> <dd>

Tipo: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\***

Puntatore a [**un oggetto ID3D11UnorderedAccessView.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)

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

[ID3DX11EffectUnorderedAccessViewVariable](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 





