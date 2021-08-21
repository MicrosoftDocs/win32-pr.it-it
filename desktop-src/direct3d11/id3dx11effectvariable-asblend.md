---
title: Metodo ID3DX11EffectVariable AsBlend (D3dx11effect.h)
description: Ottiene una variabile effect-blend.
ms.assetid: e9670d13-e006-408b-9cdf-352bcfa66a52
keywords:
- Metodo AsBlend Direct3D 11
- Metodo AsBlend Direct3D 11, interfaccia ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , AsBlend method
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsBlend
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fd9f6f76c0e3aa46e176b2f35960196fcc73eb021d4e5a250be4a5b245a5ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531603"
---
# <a name="id3dx11effectvariableasblend-method"></a>Metodo ID3DX11EffectVariable::AsBlend

Ottiene una variabile effect-blend.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectBlendVariable* AsBlend();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)\***

Puntatore a una variabile di fusione degli effetti. Vedere [**ID3DX11EffectBlendVariable.**](id3dx11effectblendvariable.md)

## <a name="remarks"></a>Commenti

AsBlend restituisce una versione della variabile dell'effetto specializzata in una variabile effect-blend. Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile dell'effetto non contiene dati di fusione degli effetti.

Le applicazioni possono testare la validità dell'oggetto restituito chiamando [**IsValid.**](id3dx11effectvariable-isvalid.md)

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

 

 





