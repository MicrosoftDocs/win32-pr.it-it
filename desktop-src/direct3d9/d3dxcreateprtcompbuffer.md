---
description: Crea un buffer PRT (Radiance Transfer) pre-ricalcolato compresso da un oggetto ID3DXPRTBuffer non compresso. Questa funzione deve essere usata con buffer per vertice o volume.
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: Funzione D3DXCreatePRTCompBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTCompBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cba1f4106a4dd04c3265bcb5cc5b19fe6a81b9ef7bd8824673e89918f9baeec4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096586"
---
# <a name="d3dxcreateprtcompbuffer-function"></a>Funzione D3DXCreatePRTCompBuffer

Crea un buffer PRT (Radiance Transfer) pre-ricalcolato compresso da un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) non compresso. Questa funzione deve essere usata con buffer per vertice o volume.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreatePRTCompBuffer(
  _In_    D3DXSHCOMPRESSQUALITYTYPE Quality,
  _In_    UINT                      NumClusters,
  _In_    UINT                      NumPCA,
  _In_    LPD3DXSHPRTSIMCB          pCB,
  _In_    LPVOID                    lpUserContext,
  _In_    LPD3DXPRTBUFFER           pBuffer,
  _Inout_ LPD3DXPRTCOMPBUFFER       *ppBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Qualità* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**

Qualità della compressione sferica aricale (SH). Vedere [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).

</dd> <dt>

*NumClusters* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di cluster da usare per la compressione.

</dd> <dt>

*NumPCA* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di vettori di base di analisi dei componenti principali (PCA) da usare in ogni cluster.

</dd> <dt>

*pCB* \[ Pollici\]
</dt> <dd>

Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Puntatore facoltativo alla funzione di callback [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) usata per calcolare la percentuale di calcoli di compressione PRT completati. La funzione di callback deve essere implementata per restituire S \_ OK per continuare a eseguire la routine di compressione. Qualsiasi altro valore interromperà la compressione. Può essere **NULL.**

</dd> <dt>

*lpUserContext* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore facoltativo a un valore definito dall'utente passato alla funzione di callback [LPD3DXSHPRTSIMCB.](lpd3dxshprtsimcb.md) Utilizzato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni di contesto per la funzione di callback. Può essere **NULL.**

</dd> <dt>

*pBuffer* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Indirizzo di un puntatore all'oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) non compresso che verrà compresso.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

Indirizzo di un puntatore [**all'oggetto ID3DXPRTCompBuffer di**](id3dxprtcompbuffer.md) output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trasferimento di radiance pre-ricalcolate](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
