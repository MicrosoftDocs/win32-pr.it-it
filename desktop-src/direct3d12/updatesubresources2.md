---
title: Funzione Updatesubresources con (allocazione heap) (D3dx12. h)
description: Aggiorna le sottorisorse con un'implementazione di allocazione dell'heap.
ms.assetid: 328D8755-D328-471D-AAF4-9771CBFF7539
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
ms.openlocfilehash: c97abe59bdd0334fe4b7badf03e44ddc03b85495
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322896"
---
# <a name="updatesubresources-heap-allocating-function"></a>Funzione Updatesubresources con (allocazione heap)

Aggiorna le sottorisorse con un'implementazione di allocazione dell'heap.

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

Puntatore all'interfaccia [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) per l'elenco dei comandi.

</dd> <dt>

*pDestinationResource* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Puntatore all'interfaccia [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) che rappresenta la risorsa di destinazione.

</dd> <dt>

*pIntermediate* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Puntatore all'interfaccia [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) che rappresenta la risorsa intermedia.

</dd> <dt>

*IntermediateOffset* 
</dt> <dd>

Tipo: **[ **UInt64**](/windows/desktop/WinProg/windows-data-types)**

Offset, in byte, della risorsa intermedia.

</dd> <dt>

*FirstSubresource* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indice della prima sottorisorsa nella risorsa. L'intervallo di valori validi è compreso tra 0 e D3D12 le \_ \_ sottorisorse di req.

</dd> <dt>

*NumSubresources* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Numero di sottorisorse nella risorsa. L'intervallo di valori validi è compreso tra 0 e (D3D12 \_ req Resources \_ - *FirstSubresource*).

</dd> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Tipo: **[ **D3D12 \_ subresource \_ Data**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***

Puntatore a una matrice (di lunghezza *NumSubresources*) di puntatori alle strutture di [**\_ \_ dati della sottorisorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) contenenti le descrizioni dei dati della sottorisorsa utilizzati per l'aggiornamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **UInt64**](/windows/desktop/WinProg/windows-data-types)**

Dimensione del buffer, in byte.

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

 

