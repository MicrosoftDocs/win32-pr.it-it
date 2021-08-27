---
title: Metodo ID3DX12PipelineParserCallbacks ErrorBadInputParameter (D3DX12.h)
description: Chiama il callback di errore del parametro di input non valido di un oggetto che implementa questa interfaccia.
ms.assetid: CB1F9A77-B120-4D72-99D3-16594E668520
keywords:
- Metodo ErrorBadInputParameter
- Metodo ErrorBadInputParameter, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo ErrorBadInputParameter
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorBadInputParameter
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91fb00490fc2c2710207e7bdd01f7be900996452f34b379a2c883ef2a99dfcd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096424"
---
# <a name="id3dx12pipelineparsercallbackserrorbadinputparameter-method"></a>Metodo ID3DX12PipelineParserCallbacks::ErrorBadInputParameter

Chiama il callback di errore del parametro di input non valido di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void ErrorBadInputParameter(
   
        UINT
           ParameterIndex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ParameterIndex* 
</dt> <dd>

Tipo: **UINT**

Posizione del parametro che contiene input non valido. Il parametro più a sinistra si trova nella posizione 1, non nella posizione 0.

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

 

 





