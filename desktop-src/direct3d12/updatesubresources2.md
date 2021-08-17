---
title: Funzione UpdateSubresources (allocazione heap) (D3dx12.h)
description: Aggiorna le sottorisorse con un'implementazione di allocazione heap.
ms.assetid: 328D8755-D328-471D-AAF4-9771CBFF7539
keywords:
- Funzione UpdateSubresources
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
ms.openlocfilehash: bc4e476501c91c3e7508c0aefdc1d9d6c99a057840b5a126879c8b4ff3608f68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460752"
---
# <a name="updatesubresources-heap-allocating-function"></a>Funzione UpdateSubresources (allocazione heap)

Aggiorna le sottorisorse con un'implementazione di allocazione heap.

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

*pCmdList* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Puntatore [**all'interfaccia ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) per l'elenco di comandi.

</dd> <dt>

*pDestinationResource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Puntatore [**all'interfaccia ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) che rappresenta la risorsa di destinazione.

</dd> <dt>

*pIntermediate* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Puntatore [**all'interfaccia ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) che rappresenta la risorsa intermedia.

</dd> <dt>

*IntermediateOffset* 
</dt> <dd>

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Offset, in byte, alla risorsa intermedia.

</dd> <dt>

*FirstSubresource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice della prima sottorisorsa nella risorsa. L'intervallo di valori validi è compreso tra 0 e D3D12 \_ REQ \_ SUBRESOURCES.

</dd> <dt>

*NumSubresources* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Numero di sottorisorse nella risorsa. L'intervallo di valori validi è compreso tra 0 e (D3D12 \_ REQ \_ SUBRESOURCES - *FirstSubresource).*

</dd> <dt>

*pSrcData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***

Puntatore a una matrice (di lunghezza *NumSubresources)* di puntatori a strutture [**\_ SUBRESOURCE \_ DATA D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) contenenti descrizioni dei dati della sottorisorsa usati per l'aggiornamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Dimensione del buffer, in byte.

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

 

