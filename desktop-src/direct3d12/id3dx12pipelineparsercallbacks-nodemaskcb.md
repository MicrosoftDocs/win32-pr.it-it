---
title: Metodo ID3DX12PipelineParserCallbacks NodemaskCb (D3DX12.h)
description: Chiama il callback del sottooggetto nodemask di un oggetto che implementa questa interfaccia.
ms.assetid: F5A408B7-A777-4BBC-A2A3-1BC3551E65ED
keywords:
- Metodo NodemaskCb
- Metodo NodemaskCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo NodemaskCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.NodemaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 356ddf6ea86980ee882ad7544096811db420ae0cf8224f315801b708b95ae98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045449"
---
# <a name="id3dx12pipelineparsercallbacksnodemaskcb-method"></a>Metodo ID3DX12PipelineParserCallbacks::NodemaskCb

Chiama il callback del sottooggetto nodemask di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void NodemaskCb(
   
        UINT
       Nodemask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Maschera di nodo* 
</dt> <dd>

Tipo: **UINT**

Dettagli del sottooggetto nodemask analizzato da un flusso di stato della pipeline.

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
</dt> </dl>

 

 





