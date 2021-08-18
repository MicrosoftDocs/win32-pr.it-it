---
title: Metodo ID3DX11EffectMatrixVariable GetMatrixTranspose (D3dx11effect.h)
description: Trasporre e ottenere una matrice a virgola mobile.
ms.assetid: a261128c-d1f9-4864-b562-5fe9a69c9969
keywords:
- Metodo GetMatrixTranspose Direct3D 11
- Metodo GetMatrixTranspose Direct3D 11, interfaccia ID3DX11EffectMatrixVariable
- ID3DX11EffectMatrixVariable interface Direct3D 11 , Metodo GetMatrixTranspose
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d2f04057dac5bc432cc3c6a9a3060654d8f6d181836823aa29f0a02f82f667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046179"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtranspose-method"></a>Metodo ID3DX11EffectMatrixVariable::GetMatrixTranspose

Trasporre e ottenere una matrice a virgola mobile.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **\* float**

Puntatore al primo elemento di una matrice trasposta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

La trasposizione di una matrice riorganizza l'ordine dei dati dall'ordine di riga-colonna all'ordine delle righe di colonna (o viceversa).

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra gli effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectMatrixVariable](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





