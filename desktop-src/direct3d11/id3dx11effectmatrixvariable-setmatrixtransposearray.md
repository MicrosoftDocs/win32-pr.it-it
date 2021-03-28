---
title: Metodo ID3DX11EffectMatrixVariable SetMatrixTransposeArray (D3dx11effect. h)
description: Trasponi e imposta una matrice di matrici a virgola mobile.
ms.assetid: 08223022-5e77-4a84-9b68-b9b0c9a02270
keywords:
- Metodo SetMatrixTransposeArray Direct3D 11
- Metodo SetMatrixTransposeArray Direct3D 11, interfaccia ID3DX11EffectMatrixVariable
- Interfaccia ID3DX11EffectMatrixVariable Direct3D 11, metodo SetMatrixTransposeArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f70676b76658b5732c1a2ee15858f83694272b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969466"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtransposearray-method"></a>Metodo ID3DX11EffectMatrixVariable:: SetMatrixTransposeArray

Trasponi e imposta una matrice di matrici a virgola mobile.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **float \***

Puntatore a una matrice di matrici.

</dd> <dt>

*Offset* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Offset (in numero di matrici) tra l'inizio della matrice e la prima matrice da impostare.

</dd> <dt>

*Count* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Numero di matrici nella matrice da impostare.

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

 

