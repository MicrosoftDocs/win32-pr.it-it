---
title: Metodo GetFloat ID3DX11EffectScalarVariable (D3dx11effect.h)
description: Ottiene una variabile a virgola mobile.
ms.assetid: 0416db40-5e70-44e4-905f-86f49a9b58b8
keywords:
- Metodo GetFloat Direct3D 11
- Metodo GetFloat Direct3D 11, interfaccia ID3DX11EffectScalarVariable
- ID3DX11EffectScalarVariable interface Direct3D 11 , Metodo GetFloat
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetFloat
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f00e5f4863b54a208b1b9f9b32e4292c274575271e447c3ac20e7b09a686ace
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952721"
---
# <a name="id3dx11effectscalarvariablegetfloat-method"></a>Metodo ID3DX11EffectScalarVariable::GetFloat

Ottiene una variabile a virgola mobile.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFloat(
   float *pValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pValue* 
</dt> <dd>

Tipo: **\* float**

Puntatore alla variabile .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra gli effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

 





