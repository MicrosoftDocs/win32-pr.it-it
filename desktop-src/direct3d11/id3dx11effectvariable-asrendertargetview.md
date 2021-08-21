---
title: Metodo ID3DX11EffectVariable AsRenderTargetView (D3dx11effect.h)
description: Ottenere una variabile render-target-view.
ms.assetid: 1eec342e-267a-4eab-886a-a309758065c7
keywords:
- Metodo AsRenderTargetView Direct3D 11
- Metodo AsRenderTargetView Direct3D 11, interfaccia ID3DX11EffectVariable
- Id3DX11EffectVariable interface Direct3D 11 , Metodo AsRenderTargetView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRenderTargetView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a8b44b3ed67b6293d4b4add329eef532fdc44cb12cea9e84b1ddf43fb72cc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531422"
---
# <a name="id3dx11effectvariableasrendertargetview-method"></a>Metodo ID3DX11EffectVariable::AsRenderTargetView

Ottenere una variabile render-target-view.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectRenderTargetViewVariable* AsRenderTargetView();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)\***

Puntatore a una variabile render-target-view. Vedere [**ID3DX11EffectRenderTargetViewVariable.**](id3dx11effectrendertargetviewvariable.md)

## <a name="remarks"></a>Commenti

Questo metodo restituisce una versione della variabile effect specializzata in una variabile render-target-view. Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile effect non contiene dati render-target-view.

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

 

 





