---
title: Metodo GetBoolVector ID3DX11EffectVectorVariable (D3dx11effect.h)
description: Ottiene un vettore a quattro componenti che contiene dati booleani.
ms.assetid: ecaf5705-d13b-4d61-9766-d2ff183af789
keywords:
- Metodo GetBoolVector Direct3D 11
- Metodo GetBoolVector Direct3D 11, interfaccia ID3DX11EffectVectorVariable
- ID3DX11EffectVectorVariable interface Direct3D 11 , Metodo GetBoolVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetBoolVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5693ffb77cc3aa2e4973f6efb168779881deafe5cab4a9c9dd869c03cb46714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124486"
---
# <a name="id3dx11effectvectorvariablegetboolvector-method"></a>Metodo ID3DX11EffectVectorVariable::GetBoolVector

Ottiene un vettore a quattro componenti che contiene dati booleani.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBoolVector(
   BOOL *pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)\***

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

 

