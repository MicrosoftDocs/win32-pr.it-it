---
description: Avviare il disegno di ogni faccia di una mappa dell'ambiente.
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: 'Metodo ID3DXRenderToEnvMap:: Face (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.Face
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 452933c0d85a7aad2987011796ff47eff41dc32b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762346"
---
# <a name="id3dxrendertoenvmapface-method"></a>Metodo ID3DXRenderToEnvMap:: Face

Avviare il disegno di ogni faccia di una mappa dell'ambiente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Faccia* \[ in\]
</dt> <dd>

Tipo: **[ **D3DCUBEMAP \_ visi**](./d3dcubemap-faces.md)**

Prima faccia della mappa del cubo ambientale. Vedere [**D3DCUBEMAP \_ visi**](./d3dcubemap-faces.md).

</dd> <dt>

*MipFilter* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione valida di uno o più flag [di \_ filtro D3DX](d3dx-filter.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato una volta per ogni tipo di mappa dell'ambiente. L'unica eccezione è rappresentata da una mappa dell'ambiente cubica che richiede che questo metodo venga chiamato sei volte, una volta per ogni viso in D3DCUBEMAP \_ visi. Per altre informazioni, vedere [mapping dell'ambiente (Direct3D 9)](environment-mapping.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
