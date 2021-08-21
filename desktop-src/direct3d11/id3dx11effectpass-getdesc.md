---
title: Metodo ID3DX11EffectPass GetDesc (D3dx11effect.h)
description: Ottenere una descrizione del pass.
ms.assetid: 423766be-96b2-4038-834e-34125789e8b1
keywords:
- Metodo GetDesc Direct3D 11
- Metodo GetDesc Direct3D 11, interfaccia ID3DX11EffectPass
- ID3DX11EffectPass interface Direct3D 11 , GetDesc method
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd75b5b23e253715af33c712fe957ae057b681f715a60fa37d4451c3fc76232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535067"
---
# <a name="id3dx11effectpassgetdesc-method"></a>Metodo ID3DX11EffectPass::GetDesc

Ottenere una descrizione del pass.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDesc(
   D3DX11_PASS_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md)\***

Puntatore a una descrizione del passaggio (vedere [**D3DX11 \_ PASS \_ DESC).**](d3dx11-pass-desc.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Un passaggio è un blocco di codice che imposta lo stato di rendering e gli shader (che a loro volta imposta buffer costanti, campionatori e trame). Una tecnica di effetto contiene uno o più passaggi.

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





