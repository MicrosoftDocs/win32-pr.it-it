---
title: Metodo ID3DX12PipelineParserCallbacks RTVFormatsCb (D3DX12.h)
description: Chiama il callback del sottooggetto della matrice di formati di destinazione di rendering di un oggetto che implementa questa interfaccia.
ms.assetid: 0D5F0BC4-D9E2-4B16-99B5-509454AF8C02
keywords:
- Metodo RTVFormatsCb
- Metodo RTVFormatsCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo RTVFormatsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RTVFormatsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d826bd2c2f3c5f1c0783a4be2cba132e4874f5a54776c227590dd87f5365d347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045439"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a>Metodo ID3DX12PipelineParserCallbacks::RTVFormatsCb

Chiama il callback del sottooggetto della matrice di formati di destinazione di rendering di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void RTVFormatsCb(
  [ref] const D3D12_RT_FORMAT_ARRAY &RTVFormats
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RTVFormats* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ RT FORMAT \_ \_ ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**

Dettagli del sottooggetto della matrice di formato di destinazione di rendering analizzato da un flusso di stato della pipeline.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Non restituisce alcun valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX12.h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce helper per Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**MATRICE DI FORMATO D3D12 \_ RT \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





