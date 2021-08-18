---
description: Ottimizza la mesh di patch per un'efficiente applicazione a più elementi.
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: Metodo ID3DXPatchMesh::Optimize (D3DX9Mesh.h)
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
ms.openlocfilehash: 245f3ddb2c85f5de6ae2acc040f929387d522c12d65eeb4d4307f162b8532af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120725"
---
# <a name="id3dxpatchmeshoptimize-method"></a>Metodo ID3DXPatchMesh::Optimize

Ottimizza la mesh di patch per un'efficiente applicazione a più elementi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Attualmente inutilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT.

## <a name="remarks"></a>Commenti

Dopo che un'applicazione genera informazioni di adizia per una mesh, i dati della mesh possono essere ottimizzati (riordinati) per migliorare le prestazioni di disegno. Questo metodo determina quali patch sono adiacenti (entro la tolleranza fornita).

Le informazioni sull'adicenza vengono usate anche per ottimizzare la rappresentazione a più elementi. Generare informazioni di adiacenza una sola volta e ripetere ripetutamente il tessellato chiamando [**ID3DXPatchMesh::Tessellate**](id3dxpatchmesh--tessellate.md). L'ottimizzazione eseguita è indipendente dal livello a più livelli effettivo usato. Tuttavia, se i vertici mesh vengono modificati, è necessario rigenerare le informazioni sull'adienza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh::GenerateAdjacency**](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 
