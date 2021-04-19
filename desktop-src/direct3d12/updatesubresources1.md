---
title: Funzione Updatesubresources con (D3dx12. h)
description: Aggiorna le sottorisorse. tutte le matrici di risorse devono essere popolate, in genere chiamando ID3D12Device GetCopyableFootprints.
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
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
ms.openlocfilehash: 885ee058aacbfca238448830f2b7b1b54a298f89
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323550"
---
# <a name="updatesubresources-function"></a>Updatesubresources con (funzione)

Aggiorna le sottorisorse, tutte le matrici di sottorisorse devono essere popolate, in genere chiamando [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).

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

*RequiredSize* 
</dt> <dd>

Tipo: **[ **UInt64**](/windows/desktop/WinProg/windows-data-types)**

Dimensioni richieste, in byte, per l'aggiornamento.

</dd> <dt>

*pLayouts* \[ in\]
</dt> <dd>

Tipo: **const \* [**D3D12 \_ POSIZIONAta \_ \_ footprint delle risorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)**

Puntatore a una matrice (di lunghezza *NumSubresources*) di puntatori alle strutture che contengono la descrizione e il posizionamento delle sottorisorse della risorsa.

</dd> <dt>

*pNumRows* \[ in\]
</dt> <dd>

Tipo: **const [**uint**](/windows/desktop/WinProg/windows-data-types) \***

Puntatore a una matrice di lunghezza *NumSubresources* di uints contenente il numero di righe per ogni sottorisorsa.

</dd> <dt>

*pRowSizesInBytes* \[ in\]
</dt> <dd>

Tipo: **const [**UInt64**](/windows/desktop/WinProg/windows-data-types) \***

Puntatore a una matrice di lunghezza *NumSubresources* di uints che contiene la dimensione, in byte, di ogni riga.

</dd> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Tipo: **const \* [**D3D12 \_ subresource \_ Data**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)**

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

 

