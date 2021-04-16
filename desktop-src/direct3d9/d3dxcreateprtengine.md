---
description: Consente di creare un oggetto ID3DXPRTEngine in grado di generare in modo efficiente simulazioni del trasferimento Radiance (pre-Computed Radiance Transfer) di una scena 3D.
ms.assetid: fdfe02b5-03fb-4bee-a53b-012ae3572644
title: Funzione D3DXCreatePRTEngine (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTEngine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b76b58953de81041922659c3315bba9cdf7788b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530930"
---
# <a name="d3dxcreateprtengine-function"></a>D3DXCreatePRTEngine (funzione)

Consente di creare un oggetto [**ID3DXPRTEngine**](id3dxprtengine.md) in grado di generare in modo efficiente simulazioni del trasferimento Radiance (pre-Computed Radiance Transfer) di una scena 3D.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreatePRTEngine(
  _In_    LPD3DXMESH      pMesh,
  _In_    DWORD           *pAdjacency,
  _In_    BOOL            ExtractUVs,
  _In_    LPD3DXMESH      pBlockerMesh,
  _Inout_ LPD3DXPRTENGINE ppEngine
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di input che modella la scena 3D. Questa mesh deve contenere una tabella di attributi in cui i vertici si trovano in un attributo univoco.

</dd> <dt>

*pAdjacency* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore facoltativo a una matrice di tre DWORD per volto da riempire con indici facciali adiacenti. Il numero di byte in questa matrice deve essere almeno ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)). Può essere **null**.

</dd> <dt>

*ExtractUVs* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **true**, verranno usate le trame per archiviare i vettori ALBEDOS o PRT.

</dd> <dt>

*pBlockerMesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) facoltativo che blocca la scena 3D. Può essere **null**.

</dd> <dt>

*ppEngine* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTENGINE**](id3dxprtengine.md)**

Puntatore a un oggetto [**ID3DXPRTEngine**](id3dxprtengine.md) di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Usare [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) per combinare più mesh in un'unica interfaccia mesh.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trasferimento Radiance pre-calcolate](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
