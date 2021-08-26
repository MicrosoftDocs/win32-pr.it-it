---
title: Metodo ID3DX11EffectVariable AsString (D3dx11effect.h)
description: Ottenere una variabile stringa.
ms.assetid: 60f8a730-bf95-4577-9259-7348d479ac3d
keywords:
- Metodo AsString Direct3D 11
- Metodo AsString Direct3D 11, interfaccia ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , Metodo AsString
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c69eecaabec6b7da49f7f36f6c75677fdd20cdb462f26fe5e02650e6746c01f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069611"
---
# <a name="id3dx11effectvariableasstring-method"></a>Metodo ID3DX11EffectVariable::AsString

Ottenere una variabile stringa.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectStringVariable* AsString();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)\***

Puntatore a una variabile stringa. Vedere [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md).

## <a name="remarks"></a>Commenti

AsString restituisce una versione della variabile effect specializzata in una variabile stringa. Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile effect non contiene dati stringa.

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

 

 





