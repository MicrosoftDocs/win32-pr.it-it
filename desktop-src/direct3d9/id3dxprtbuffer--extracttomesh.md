---
description: Estrae i dati del coefficiente da un buffer a canale singolo e li aggiunge a un oggetto ID3DXMesh.
ms.assetid: 4fada987-ddd7-4c02-a177-dd81f3790588
title: Metodo ID3DXPRTBuffer::ExtractToMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c838a146a390aa72ac24781ca6f136b028ad41a6ee94fb4210ec4bd3f557acdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120615"
---
# <a name="id3dxprtbufferextracttomesh-method"></a>Metodo ID3DXPRTBuffer::ExtractToMesh

Estrae i dati del coefficiente da un buffer a canale singolo e li aggiunge a [**un oggetto ID3DXMesh.**](id3dxmesh.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumCoefficients,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NumCoefficients* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di coefficienti da estrarre dal buffer. Quando si usa il trasferimento della radice pre-ricalcolata sferica (SH), il numero di coefficienti deve essere Order PIÙ. L'ordine deve essere compreso nell'intervallo [da D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusi.

</dd> <dt>

*Utilizzo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Descrizioni dell'utilizzo dei vertici della mesh. Vedere [**D3DDECLUSAGE.**](./d3ddeclusage.md)

</dd> <dt>

*UsageIndexStart* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice iniziale per i coefficienti da archiviare nella mesh.

</dd> <dt>

*pScene* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) che archivierà i coefficienti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
