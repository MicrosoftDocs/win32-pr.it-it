---
title: Metodo ID3DX11EffectVectorVariable SetFloatVector (D3dx11effect. h)
description: Impostare un vettore a quattro componenti che contiene dati a virgola mobile.
ms.assetid: fb646df6-b9f9-4d71-93c3-38833076b781
keywords:
- Metodo SetFloatVector Direct3D 11
- Metodo SetFloatVector Direct3D 11, interfaccia ID3DX11EffectVectorVariable
- Interfaccia ID3DX11EffectVectorVariable Direct3D 11, metodo SetFloatVector
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
ms.openlocfilehash: c5541f2773e992c4c52bf748bceb832d67b28825
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401999"
---
# <a name="id3dx11effectvectorvariablesetfloatvector-method"></a>Metodo ID3DX11EffectVectorVariable:: SetFloatVector

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

Tipo: **float \***

Puntatore al primo componente.

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

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

 





