---
title: Funzione UpdateSubresources (D3dx12.h)
description: Aggiorna le sottorisorse. Tutte le matrici di sottorisorse devono essere popolate, in genere chiamando ID3D12Device GetCopyableFootprints.
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
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
ms.openlocfilehash: bb1e48f4bc574d0b032b878c19c7749f63f86aba21a659c1c0a8f6f526f5bce5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496601"
---
# <a name="updatesubresources-function"></a>Funzione UpdateSubresources

Aggiorna le sottorisorse, tutte le matrici di sottorisorse devono essere popolate, in genere chiamando [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).

## <a name="syntax"></a>Sintassi


```C++
UINT64 inline UpdateSubresources(
  _In_       ID3D12GraphicsCommandList          *pCmdList,
  _In_       ID3D12Resource                     *pDestinationResource,
  _In_       ID3D12Resource                     *pIntermediate,
  _In_       UINT                               FirstSubresource,
  _In_       UINT                               NumSubresources,
             UINT64                             RequiredSize,
  _In_ const D3D12_PLACED_SUBRESOURCE_FOOTPRINT *pLayouts,
  _In_ const UINT                               *pNumRows,
  _In_ const UINT64                             *pRowSizesInBytes,
  _In_ const D3D12_SUBRESOURCE_DATA             *pSrcData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCmdList* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Elenco di comandi, come puntatore a [**un ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).

</dd> <dt>

*pDestinationResource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Risorsa di destinazione, come puntatore a [**un oggetto ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).

</dd> <dt>

*pIntermediate* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Risorsa intermedia, come puntatore a [**id3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).

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

*RequiredSize* 
</dt> <dd>

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Dimensioni richieste, in byte, per l'aggiornamento.

</dd> <dt>

*pLayouts* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3D12 \_ PLACED \_ SUBRESOURCE \_ FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) \***

Puntatore a una matrice (di lunghezza *NumSubresources)* di puntatori alle strutture che contiene la descrizione e la posizione delle sottorisorse della risorsa.

</dd> <dt>

*pNumRows* \[ Pollici\]
</dt> <dd>

Tipo: **const [**UINT**](/windows/desktop/WinProg/windows-data-types) \***

Puntatore a una matrice (di lunghezza *NumSubresources)* di UINTS contenente il numero di righe per ogni sottorisorsa.

</dd> <dt>

*pRowSizesInBytes* \[ Pollici\]
</dt> <dd>

Tipo: **const [**UINT64**](/windows/desktop/WinProg/windows-data-types) \***

Puntatore a una matrice (di lunghezza *NumSubresources)* di UINTS contenente le dimensioni, in byte, di ogni riga.

</dd> <dt>

*pSrcData* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***

Puntatore a una matrice (di lunghezza *NumSubresources)* di puntatori a strutture [**D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) contenenti descrizioni dei dati di sottorisorsa usati per l'aggiornamento.

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

 

