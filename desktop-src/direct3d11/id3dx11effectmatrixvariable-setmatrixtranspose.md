---
title: Metodo ID3DX11EffectMatrixVariable SetMatrixTranspose (D3dx11effect. h)
description: Trasponi e imposta una matrice a virgola mobile.
ms.assetid: 228546c9-0141-4e17-bc8f-bff7201825d7
keywords:
- Metodo SetMatrixTranspose Direct3D 11
- Metodo SetMatrixTranspose Direct3D 11, interfaccia ID3DX11EffectMatrixVariable
- Interfaccia ID3DX11EffectMatrixVariable Direct3D 11, metodo SetMatrixTranspose
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daf77b6e2e9578dcbc6c9cfe80f57b149097c32
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982259"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtranspose-method"></a>Metodo ID3DX11EffectMatrixVariable:: SetMatrixTranspose

Trasponi e imposta una matrice a virgola mobile.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **float \***

Puntatore al primo elemento di una matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Se si traspone una matrice, l'ordine dei dati viene riorganizzato dall'ordine delle colonne di riga a quello delle righe di colonna (o viceversa).

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectMatrixVariable](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





