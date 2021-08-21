---
title: Metodo ID3DX11EffectVariable AsScalar (D3dx11effect.h)
description: Ottenere una variabile scalare.
ms.assetid: 5cc02fb3-351a-4309-9145-1ed7d759a650
keywords:
- Metodo AsScalar Direct3D 11
- Metodo AsScalar Direct3D 11, interfaccia ID3DX11EffectVariable
- INTERFACCIA ID3DX11EffectVariable Direct3D 11, metodo AsScalar
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsScalar
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 704002e17d963897111949f559c4798c433c3d939946a735362876fa2e22f7ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531412"
---
# <a name="id3dx11effectvariableasscalar-method"></a>Metodo ID3DX11EffectVariable::AsScalar

Ottenere una variabile scalare.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectScalarVariable* AsScalar();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)\***

Puntatore a una variabile scalare. Vedere [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md).

## <a name="remarks"></a>Commenti

AsScalar restituisce una versione della variabile di effetto specializzata in una variabile scalare. Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile effect non contiene dati scalari.

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

 

 





