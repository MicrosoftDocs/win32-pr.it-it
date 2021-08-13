---
title: Metodo SetInt ID3DX11EffectScalarVariable (D3dx11effect.h)
description: Impostare una variabile integer.
ms.assetid: 614284be-8f70-4d7e-b797-b67e813615ab
keywords:
- Metodo SetInt Direct3D 11
- Metodo SetInt Direct3D 11, interfaccia ID3DX11EffectScalarVariable
- ID3DX11EffectScalarVariable interface Direct3D 11 , SetInt method
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetInt
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 215083d35bfbdd67cd970bfe31b81a1e19594b2bf849e1c19692fa96af257036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119377541"
---
# <a name="id3dx11effectscalarvariablesetint-method"></a>Metodo ID3DX11EffectScalarVariable::SetInt

Impostare una variabile integer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetInt(
   int Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Valore* 
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Puntatore alla variabile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

