---
title: Funzione D3D12GetFormatPlaneCount (D3dx12. h)
description: Ottiene il numero di piani per il formato DXGI specificato per la scheda virtuale specificata (ID3D12Device).
ms.assetid: CD21F6F9-A9AA-4CE8-A430-57C70326CB4B
keywords:
- D3D12GetFormatPlaneCount (funzione)
topic_type:
- apiref
api_name:
- D3D12GetFormatPlaneCount
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2e88c162068de2b97c9df5071398e2fab068
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322178"
---
# <a name="d3d12getformatplanecount-function"></a>D3D12GetFormatPlaneCount (funzione)

Ottiene il numero di piani per il formato DXGI specificato per la scheda virtuale specificata ( **ID3D12Device**).

## <a name="syntax"></a>Sintassi


```C++
UINT8 inline D3D12GetFormatPlaneCount(
  _In_ ID3D12Device *pDevice,
       DXGI_FORMAT  Format
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***

Scheda virtuale ( [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) per cui ottenere il conteggio del piano.

</dd> <dt>

*Formato* 
</dt> <dd>

Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

[**\_ Formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) per il quale ottenere il conteggio del piano.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **Uint8**

Il numero di piani per il formato specificato nella scheda virtuale specificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Informazioni sul \_ formato dei dati della funzionalità \_ D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)
</dt> <dt>

[**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
</dt> <dt>

[Funzioni helper per D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

