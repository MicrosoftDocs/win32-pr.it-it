---
description: Ottimizza la mesh della patch per un efficiente mosaico.
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: 'Metodo ID3DXPatchMesh:: Optimize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fa66aadd0ef1f9f9f65747694fc311f80172449
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969518"
---
# <a name="id3dxpatchmeshoptimize-method"></a>Metodo ID3DXPatchMesh:: Optimize

Ottimizza la mesh della patch per un efficiente mosaico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Attualmente non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT.

## <a name="remarks"></a>Commenti

Quando un'applicazione genera informazioni adiacenza per una mesh, i dati della mesh possono essere ottimizzati (riordinati) per migliorare le prestazioni del disegno. Questo metodo determina quali patch sono adiacenti (entro la tolleranza fornita).

Le informazioni adiacenza vengono usate anche per ottimizzare la suddivisione a mosaico. Generare le informazioni adiacenza una sola volta e conteggiarla suddividerla ripetutamente chiamando [**ID3DXPatchMesh:: conteggiarla suddividerla**](id3dxpatchmesh--tessellate.md). L'ottimizzazione eseguita è indipendente dal livello di mosaico effettivo utilizzato. Tuttavia, se i vertici della mesh vengono modificati, è necessario rigenerare le informazioni adiacenza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh:: GenerateAdjacency**](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 
