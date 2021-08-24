---
description: Restituisce una mesh con modifiche risultanti dal campionamento spaziale adattivo. La mesh restituita contiene solo posizioni, normali e coordinate di trama (se definite).
ms.assetid: 21447733-b27b-4906-8c0e-7089dec71b5b
title: Metodo ID3DXPRTEngine::GetAdaptedMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetAdaptedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5e38937628bc36f49059bcb3e798a6d13e538c572c1c5fb6ef20865ed05385d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747671"
---
# <a name="id3dxprtenginegetadaptedmesh-method"></a>Metodo ID3DXPRTEngine::GetAdaptedMesh

Restituisce una mesh con modifiche risultanti dal campionamento spaziale adattivo. La mesh restituita contiene solo posizioni, normali e coordinate di trama (se definite).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAdaptedMesh(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in, out] UINT              *pFaceRemap,
  [in, out] UINT              *pVertRemap,
  [in, out] FLOAT             *pfVertWeights,
  [out]     LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un dispositivo IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) usato per creare la mesh di output.

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntatore alla faccia mesh originale divisa per generare la faccia corrente.

</dd> <dt>

*pVertRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di destinazione contenente i tre vertici di mesh originali che sono gli elementi padre del vertice corrente.

</dd> <dt>

*pfVertWeights* \[ in, out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di destinazione contenente i fattori di fusione per i vertici pVertRemap.

</dd> <dt>

*ppMesh* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Puntatore all'oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Commenti

pVertRemap e pfVertWeights possono essere usati per interpolare qualsiasi valore per vertice nella mesh.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
