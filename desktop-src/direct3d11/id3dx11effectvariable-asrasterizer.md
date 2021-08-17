---
title: Metodo ID3DX11EffectVariable AsRasterizer (D3dx11effect.h)
description: Ottenere una variabile di rasterizzazione.
ms.assetid: 6a55d067-f527-4a1b-a4d4-a6d1719aebe7
keywords:
- Metodo AsRasterizer Direct3D 11
- Metodo AsRasterizer Direct3D 11, interfaccia ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , Metodo AsRasterizer
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRasterizer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfaf83debc6c7e73a89f78b0c8c3899cce2fb83fb6a5884fa5a5ed9ed5b35912
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858101"
---
# <a name="id3dx11effectvariableasrasterizer-method"></a>Metodo ID3DX11EffectVariable::AsRasterizer

Ottenere una variabile di rasterizzazione.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectRasterizerVariable* AsRasterizer();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)\***

Puntatore a una variabile di rasterizzazione. Vedere [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md).

## <a name="remarks"></a>Commenti

AsRasterizer restituisce una versione della variabile dell'effetto specializzata in una variabile di rasterizzazione. Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile dell'effetto non contiene dati del rasterizzatore.

Le applicazioni possono testare la validità dell'oggetto restituito chiamando [**IsValid**](id3dx11effectvariable-isvalid.md).

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





