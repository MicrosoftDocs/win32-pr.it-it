---
title: Metodo getdesc ID3DX11EffectTechnique (D3dx11effect. h)
description: Ottenere una descrizione tecnica.
ms.assetid: ed82d873-0540-4aa8-ac0f-198852b886ad
keywords:
- Metodo getdesc Direct3D 11
- Metodo getdesc Direct3D 11, interfaccia ID3DX11EffectTechnique
- Interfaccia ID3DX11EffectTechnique Direct3D 11, metodo getdesc
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b847bd8381ec7d190931c04e5940f713676ff0b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995840"
---
# <a name="id3dx11effecttechniquegetdesc-method"></a>Metodo ID3DX11EffectTechnique:: getdesc

Ottenere una descrizione tecnica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDesc(
   D3DX11_TECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ Technique \_ desc**](d3dx11-technique-desc.md)\***

Puntatore a una descrizione di tecnica (vedere [**D3DX11 \_ Technique \_ desc**](d3dx11-technique-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

 





