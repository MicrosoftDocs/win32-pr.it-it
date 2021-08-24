---
title: Metodo ID3DX11EffectScalarVariable SetFloat (D3dx11effect.h)
description: Impostare una variabile a virgola mobile.
ms.assetid: e13f3ba1-437a-47f0-bd08-4423ffc25ddb
keywords:
- Metodo SetFloat Direct3D 11
- Metodo SetFloat Direct3D 11, interfaccia ID3DX11EffectScalarVariable
- ID3DX11EffectScalarVariable interface Direct3D 11 , SetFloat method
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetFloat
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 573880f07752e353e7a623d249353f7e0f020902443fde23538f38a2227e7d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460851"
---
# <a name="id3dx11effectscalarvariablesetfloat-method"></a>Metodo ID3DX11EffectScalarVariable::SetFloat

Impostare una variabile a virgola mobile.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetFloat(
   float Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Valore* 
</dt> <dd>

Tipo: **float**

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

 

 





