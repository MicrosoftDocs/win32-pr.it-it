---
title: Metodo ID3DX12PipelineParserCallbacks RTVFormatsCb (D3DX12. h)
description: Chiama il callback del sottooggetto della matrice del formato della destinazione di rendering di un oggetto che implementa questa interfaccia.
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
ms.openlocfilehash: caaa1df508e1a448de3851d408f9aad5ac94d957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323094"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a>Metodo ID3DX12PipelineParserCallbacks:: RTVFormatsCb

Chiama il callback del sottooggetto della matrice del formato della destinazione di rendering di un oggetto che implementa questa interfaccia.

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

Tipo: **const [**D3D12 \_ RT \_ Format \_ Array**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**

Dettagli del sottooggetto di matrice del formato della destinazione di rendering analizzato da un flusso di stato della pipeline.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Non restituisce alcun elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX12. h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce helper per Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**\_Matrice di \_ formato D3D12 RT \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





