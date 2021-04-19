---
description: Ridimensiona tutti gli esempi associati a una data mesh specificata. Il metodo è utile per il calcolo della dispersione della sottosuperficie.
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: 'Metodo ID3DXPRTEngine:: ScaleMeshChunk (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ScaleMeshChunk
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f688a5175e7b50c33dd93d06a4f988a14c062c86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323436"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a>Metodo ID3DXPRTEngine:: ScaleMeshChunk

Ridimensiona tutti gli esempi associati a una data mesh specificata. Il metodo è utile per il calcolo della dispersione della sottosuperficie.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ScaleMeshChunk(
  [in]      UINT            uMeshChunk,
  [in]      FLOAT           fScale,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uMeshChunk* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Posizione nella rete in cui iniziare il ridimensionamento degli esempi.

</dd> <dt>

*fScale* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valore in base al quale moltiplicare ogni vettore nel sottomesh.

</dd> <dt>

*pDataOut* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) per ricevere esempi riscalati nel sottomesh.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
