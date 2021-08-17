---
title: Metodo ID3DX11EffectVariable GetParentConstantBuffer (D3dx11effect.h)
description: Ottiene un buffer costante. | Metodo ID3DX11EffectVariable GetParentConstantBuffer (D3dx11effect.h)
ms.assetid: 43b46b05-951e-4c52-8bc7-4bb5f657ea78
keywords:
- Metodo GetParentConstantBuffer Direct3D 11
- Metodo GetParentConstantBuffer Direct3D 11, interfaccia ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , GetParentConstantBuffer method
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetParentConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2319a72e50d83f3780b68de163dc370d5627c28ab4ab84f6621c11faf6df7805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734114"
---
# <a name="id3dx11effectvariablegetparentconstantbuffer-method"></a>Metodo ID3DX11EffectVariable::GetParentConstantBuffer

Ottiene un buffer costante.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectConstantBuffer* GetParentConstantBuffer();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Puntatore a [**id3DX11EffectConstantBuffer.**](id3dx11effectconstantbuffer.md)

## <a name="remarks"></a>Commenti

Le variabili di effetto sono lette da o scritte in un buffer costante.

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





