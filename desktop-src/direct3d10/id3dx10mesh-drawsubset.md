---
description: Disegna un subset di una mesh.
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: Metodo ID3DX10Mesh::D rawSubset (D3DX10. h)
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
ms.openlocfilehash: 80beceebeead84a782cc7852ac0d2fe15ad61ff3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322752"
---
# <a name="id3dx10meshdrawsubset-method"></a>ID3DX10Mesh::D Metodo rawSubset

Disegna un subset di una mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AttribId* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Specifica il subset della mesh da creare. Questo valore viene utilizzato per distinguere i visi in una mesh come appartenenti a uno o più gruppi di attributi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Una tabella degli attributi viene utilizzata per identificare le aree della mesh che devono essere disegnate con trame, Stati di rendering, materiali e così via. Inoltre, l'applicazione può usare la tabella attribute per nascondere parti di una mesh senza disegnare un identificatore di attributo specificato (AttribId) durante il disegno del frame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
