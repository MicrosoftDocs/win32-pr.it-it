---
title: Metodo ID3DX11Effect GetVariableBySemantic (D3dx11effect. h)
description: Ottenere una variabile in base alla semantica.
ms.assetid: fe731af6-3e9b-4f3e-9761-121796ac8c48
keywords:
- Metodo GetVariableBySemantic Direct3D 11
- Metodo GetVariableBySemantic Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetVariableBySemantic
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8276b1850242bd83639883bf75fc927d8484765
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235148"
---
# <a name="id3dx11effectgetvariablebysemantic-method"></a>Metodo ID3DX11Effect:: GetVariableBySemantic

Ottenere una variabile in base alla semantica.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectVariable* GetVariableBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Semantica* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome semantico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntatore alla variabile Effect indicata dalla semantica. Vedere [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Commenti

Ogni variabile Effect può avere una semantica collegata, ovvero una stringa di metadati definita dall'utente. Alcune [semantiche dei valori di sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) sono parole riservate che attivano funzionalità predefinite per fasi della pipeline.

Il metodo restituisce un puntatore a un' [**interfaccia di variabile di effetto**](id3dx11effectvariable.md) se non viene trovata una variabile. è possibile chiamare [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) per verificare se la semantica esiste o meno.

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

