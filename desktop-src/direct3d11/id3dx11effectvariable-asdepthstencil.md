---
title: Metodo ID3DX11EffectVariable AsDepthStencil (D3dx11effect.h)
description: Ottenere una variabile depth-stencil.
ms.assetid: 3526812b-6c43-492e-b529-12f61ecd20e3
keywords:
- Metodo AsDepthStencil Direct3D 11
- Metodo AsDepthStencil Direct3D 11, interfaccia ID3DX11EffectVariable
- Id3DX11EffectVariable interface Direct3D 11 , Metodo AsDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771f22b6b757b9144fca7e2637a3a702232b3d2a4a837938454b2acd5237cfae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729131"
---
# <a name="id3dx11effectvariableasdepthstencil-method"></a>Metodo ID3DX11EffectVariable::AsDepthStencil

Ottenere una variabile depth-stencil.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectDepthStencilVariable* AsDepthStencil();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)\***

Puntatore a una variabile depth-stencil. Vedere [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md).

## <a name="remarks"></a>Commenti

AsDepthStencil restituisce una versione della variabile effect specializzata in una variabile depth-stencil. Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile effect non contiene dati depth-stencil.

Le applicazioni possono testare la validità dell'oggetto restituito chiamando [**IsValid**](id3dx11effectvariable-isvalid.md).

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra gli effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





