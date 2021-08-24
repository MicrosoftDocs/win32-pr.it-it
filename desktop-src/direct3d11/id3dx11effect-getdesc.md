---
title: Metodo GetDesc ID3DX11Effect (D3dx11effect.h)
description: Ottenere una descrizione dell'effetto.
ms.assetid: ca684786-c813-48d1-acad-e78aafd1c0db
keywords:
- Metodo GetDesc Direct3D 11
- Metodo GetDesc Direct3D 11, interfaccia ID3DX11Effect
- INTERFACCIA ID3DX11Effect Direct3D 11, metodo GetDesc
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9461dafb6b8da66ffa2a84e0d9d61c119a67c33bd967ae5183252e875fb6192
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676951"
---
# <a name="id3dx11effectgetdesc-method"></a>Metodo ID3DX11Effect::GetDesc

Ottenere una descrizione dell'effetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ EFFECT \_ DESC**](d3dx11-effect-desc.md)\***

Puntatore a una descrizione dell'effetto (vedere [**D3DX11 \_ EFFECT \_ DESC).**](d3dx11-effect-desc.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Una descrizione dell'effetto contiene informazioni di base su un effetto, ad esempio le tecniche contenute e le risorse del buffer costanti richieste.

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra gli effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 





