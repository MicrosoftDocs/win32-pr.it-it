---
title: Metodo ID3DX11EffectVectorVariable SetFloatVector (D3dx11effect.h)
description: Impostare un vettore a quattro componenti che contiene dati a virgola mobile.
ms.assetid: fb646df6-b9f9-4d71-93c3-38833076b781
keywords:
- Metodo SetFloatVector Direct3D 11
- Metodo SetFloatVector Direct3D 11, interfaccia ID3DX11EffectVectorVariable
- ID3DX11EffectVectorVariable interface Direct3D 11 , SetFloatVector method
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetFloatVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eabbe600b645069786eeadd082e1653875b845593788a4cdf315e120670ca0c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734003"
---
# <a name="id3dx11effectvectorvariablesetfloatvector-method"></a>Metodo ID3DX11EffectVectorVariable::SetFloatVector

Impostare un vettore a quattro componenti che contiene dati a virgola mobile.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetFloatVector(
   float *pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **\* float**

Puntatore al primo componente.

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

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

 





