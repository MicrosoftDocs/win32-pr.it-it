---
description: 'Metodo ID3DX10Mesh::D rawSubset: disegna un subset di una mesh.'
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: Metodo ID3DX10Mesh::D rawSubset (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 75723819ab7a4f82f25a68dfc2f0017e8b871130a8e0fbe70c939a95de221426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753101"
---
# <a name="id3dx10meshdrawsubset-method"></a>Metodo ID3DX10Mesh::D rawSubset

Disegna un subset di una mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AttribId* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Specifica il subset della mesh da disegnare. Questo valore viene usato per distinguere i visi in una mesh come appartenenti a uno o più gruppi di attributi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in Codici restituiti [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Una tabella di attributi viene usata per identificare le aree della mesh che devono essere disegnate con trame, stati di rendering, materiali e così via diversi. Inoltre, l'applicazione può usare la tabella degli attributi per nascondere parti di una mesh non disegnando un determinato identificatore di attributo (AttribId) durante il disegno del frame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
