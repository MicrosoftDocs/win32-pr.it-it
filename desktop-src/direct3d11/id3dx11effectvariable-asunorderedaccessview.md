---
title: Metodo ID3DX11EffectVariable AsUnorderedAccessView (D3dx11effect.h)
description: Ottenere una variabile unordered-access-view.
ms.assetid: e8b7c104-09f7-4bfb-9980-a5603550b723
keywords:
- Metodo AsUnorderedAccessView Direct3D 11
- Metodo AsUnorderedAccessView Direct3D 11, interfaccia ID3DX11EffectVariable
- Id3DX11EffectVariable interface Direct3D 11 , Metodo AsUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4cf3a1f146af7ca6faf3ff3e704285ac19f01a117809429842b45df9b7dcfd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531209"
---
# <a name="id3dx11effectvariableasunorderedaccessview-method"></a>Metodo ID3DX11EffectVariable::AsUnorderedAccessView

Ottenere una variabile unordered-access-view.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectUnorderedAccessViewVariable* AsUnorderedAccessView();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***

Puntatore a una variabile unordered-access-view. Vedere [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md).

## <a name="remarks"></a>Commenti

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

 

 





