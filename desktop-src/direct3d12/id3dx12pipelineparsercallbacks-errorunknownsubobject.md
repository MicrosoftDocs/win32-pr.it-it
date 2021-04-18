---
title: Metodo ID3DX12PipelineParserCallbacks ErrorUnknownSubobject (D3DX12. h)
description: Chiama il callback di errore del sottooggetto sconosciuto di un oggetto che implementa questa interfaccia.
ms.assetid: 612D7C44-4DC5-4DEA-B369-09C27123D45E
keywords:
- Metodo ErrorUnknownSubobject
- Metodo ErrorUnknownSubobject, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo ErrorUnknownSubobject
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorUnknownSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e294e3face085c5298f3cc624d7c0ef70dcf865
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323109"
---
# <a name="id3dx12pipelineparsercallbackserrorunknownsubobject-method"></a>Metodo ID3DX12PipelineParserCallbacks:: ErrorUnknownSubobject

Chiama il callback di errore del sottooggetto sconosciuto di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void ErrorUnknownSubobject(
   
        UINT
           UnknownTypeValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UnknownTypeValue* 
</dt> <dd>

Tipo: **uint**

Tipo di sottooggetto non riconosciuto del tentativo del sottooggetto.

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
</dt> </dl>

 

 





