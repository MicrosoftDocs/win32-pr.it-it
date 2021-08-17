---
title: Funzione MemcpySubresource (D3dx12.h)
description: Copia una sottorisorsa riga per riga.
ms.assetid: 33A9F99D-FD85-4FD6-AFD6-7A10F16C3D9B
keywords:
- Funzione MemcpySubresource
topic_type:
- apiref
api_name:
- MemcpySubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c27e8cf9ffda237c2dad017b3a981ff71498a22c1c7b54ede032d6bf8c012a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733363"
---
# <a name="memcpysubresource-function"></a>Funzione MemcpySubresource

Copia una sottorisorsa riga per riga.

## <a name="syntax"></a>Sintassi


```C++
void inline MemcpySubresource(
  _In_ const D3D12_MEMCPY_DEST      *pDest,
  _In_ const D3D12_SUBRESOURCE_DATA *pSrc,
             SIZE_T                 RowSizeInBytes,
             UINT                   NumRows,
             UINT                   NumSlices
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDest* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3D12 \_ MEMCPY \_ DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) \***

Puntatore a una [**struttura DEST D3D12 \_ MEMCPY \_ che**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) descrive la destinazione dell'operazione di copia della memoria.

</dd> <dt>

*pSrc* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***

Puntatore a una [**struttura D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) che descrive l'origine dell'operazione di copia della memoria.

</dd> <dt>

*RowSizeInBytes* 
</dt> <dd>

Tipo: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Dimensioni, in byte, di ogni riga.

</dd> <dt>

*NumRows* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Numero di righe.

</dd> <dt>

*NumSlices* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Numero di sezioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Considerare anche i metodi seguenti:

-   [**ID3D12Resource::WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)
-   [**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)
-   [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper per D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Sottorisorse](subresources.md)
</dt> </dl>

 

