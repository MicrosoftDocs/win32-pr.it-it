---
title: Funzione Updatesubresources con (stack-allocating) (D3dx12. h)
description: Aggiorna le sottorisorse con un'implementazione di allocazione dello stack.
ms.assetid: 2F30FDF1-4450-473E-AEA8-C5FF54260BCE
keywords:
- Updatesubresources con (funzione)
topic_type:
- apiref
api_name:
- UpdateSubresources
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 237e7df26b35b4cb5b1dba7b2a80c1baaac64e8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322382"
---
# <a name="updatesubresources-stack-allocating-function"></a>Funzione Updatesubresources con (stack-allocazione)

Aggiorna le sottorisorse con un'implementazione di allocazione dello stack.

## <a name="syntax"></a>Sintassi


```C++
UINT64 inline UpdateSubresources(
  _In_ ID3D12GraphicsCommandList *pCmdList,
  _In_ ID3D12Resource            *pDestinationResource,
  _In_ ID3D12Resource            *pIntermediate,
       UINT64                    IntermediateOffset,
  _In_ UINT                      FirstSubresource,
  _In_ UINT                      NumSubresources,
  _In_ D3D12_SUBRESOURCE_DATA    *pSrcData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCmdList* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Elenco di comandi, come puntatore a un [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).

</dd> <dt>

*pDestinationResource* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Risorsa di destinazione, come puntatore a un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).

</dd> <dt>

*pIntermediate* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Risorsa intermedia, come puntatore a un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).

</dd> <dt>

*IntermediateOffset* 
</dt> <dd>

Tipo: **[ **UInt64**](/windows/desktop/WinProg/windows-data-types)**

Offset, in byte, della risorsa intermedia.

</dd> <dt>

*FirstSubresource* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indice della prima sottorisorsa nella risorsa. I valori validi sono compresi tra 0 e *MaxSubresources*.

</dd> <dt>

*NumSubresources* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Numero di sottorisorse nella risorsa. I valori validi sono compresi tra 1 e (*MaxSubresources*  -  *FirstSubresource*).

</dd> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Tipo: **[ **D3D12 \_ subresource \_ Data**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***

Puntatore a una matrice (di lunghezza *NumSubresources*) di puntatori alle strutture di [**\_ \_ dati della sottorisorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) contenenti le descrizioni dei dati della sottorisorsa utilizzati per l'aggiornamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **UInt64**](/windows/desktop/WinProg/windows-data-types)**

Dimensione del buffer, in byte.

## <a name="remarks"></a>Commenti

La dichiarazione di questa funzione inizia con: `template <UINT MaxSubresources>`

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper per D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Sottorisorse](subresources.md)
</dt> </dl>

 

