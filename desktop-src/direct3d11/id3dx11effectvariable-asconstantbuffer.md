---
title: Metodo ID3DX11EffectVariable AsConstantBuffer (D3dx11effect.h)
description: Ottiene un buffer costante. | Metodo ID3DX11EffectVariable AsConstantBuffer (D3dx11effect.h)
ms.assetid: b8d8b43c-4626-43b6-8a49-8ffa7cb48427
keywords:
- Metodo AsConstantBuffer Direct3D 11
- Metodo AsConstantBuffer Direct3D 11, interfaccia ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , AsConstantBuffer method
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b232a9eb98b4cb5bdd4137661198abb9b853faa126579bd86c69e8dce375a6f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531575"
---
# <a name="id3dx11effectvariableasconstantbuffer-method"></a>Metodo ID3DX11EffectVariable::AsConstantBuffer

Ottiene un buffer costante.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectConstantBuffer* AsConstantBuffer();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Puntatore a un buffer costante. Vedere [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Commenti

AsConstantBuffer restituisce una versione della variabile dell'effetto specializzata in un buffer costante. Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile dell'effetto non contiene dati costanti del buffer.

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

 

 





