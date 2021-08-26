---
title: Metodo GetIntVector ID3DX11EffectVectorVariable (D3dx11effect.h)
description: Ottiene un vettore a quattro componenti che contiene dati integer.
ms.assetid: 27c75cfb-7c6f-43f4-9489-186006a60203
keywords:
- Metodo GetIntVector Direct3D 11
- Metodo GetIntVector Direct3D 11, interfaccia ID3DX11EffectVectorVariable
- INTERFACCIA ID3DX11EffectVectorVariable Direct3D 11, metodo GetIntVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetIntVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f41ffed10307cbf836c87506ae5dc97e1db314acce0b1cf03ebe77baafc1404
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952711"
---
# <a name="id3dx11effectvectorvariablegetintvector-method"></a>Metodo ID3DX11EffectVectorVariable::GetIntVector

Ottiene un vettore a quattro componenti che contiene dati integer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIntVector(
   int *pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

Puntatore al primo componente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

