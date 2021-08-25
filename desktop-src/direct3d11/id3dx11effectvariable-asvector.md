---
title: Metodo ID3DX11EffectVariable AsVector (D3dx11effect.h)
description: Ottenere una variabile vettore.
ms.assetid: 995bd9f3-1417-4048-9a23-4dcb3864c77d
keywords:
- Metodo AsVector Direct3D 11
- Metodo AsVector Direct3D 11, interfaccia ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , Metodo AsVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd5ce5023c0fd77109d91705c3faaf788b5f0e6edd3bd3ba15b7aeb367b8d061
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119691"
---
# <a name="id3dx11effectvariableasvector-method"></a>Metodo ID3DX11EffectVariable::AsVector

Ottenere una variabile vettore.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectVectorVariable* AsVector();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)\***

Puntatore a una variabile vettore. Vedere [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md).

## <a name="remarks"></a>Commenti

AsVector restituisce una versione della variabile dell'effetto specializzata in una variabile vettore. Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile effect non contiene dati vettoriali.

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

 

 





