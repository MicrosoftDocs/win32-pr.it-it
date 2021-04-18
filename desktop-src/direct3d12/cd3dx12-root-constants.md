---
title: Struttura CD3DX12_ROOT_CONSTANTS (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura di costanti radice D3D12 \_ .
ms.assetid: 2F517DCE-BC0C-4678-9C25-D826036F99A8
keywords:
- Struttura CD3DX12_ROOT_CONSTANTS
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_CONSTANTS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a1f81a429b083400adad60f316cc90c4ede1d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322212"
---
# <a name="cd3dx12_root_constants-structure"></a>\_Struttura delle \_ costanti radice CD3DX12

Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ costanti radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_ROOT_CONSTANTS  : public D3D12_ROOT_CONSTANTS{
       CD3DX12_ROOT_CONSTANTS();
       explicit CD3DX12_ROOT_CONSTANTS(const D3D12_ROOT_CONSTANTS &o);
       CD3DX12_ROOT_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Costanti CD3DX12 radice \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ costante CD3DX12 radice \_ .

</dd> <dt>

**costanti radice CD3DX12 esplicite \_ \_ (costanti D3D12 \_ radice \_ costanti &o)**
</dt> <dd>

Crea una nuova istanza di una \_ costante CD3DX12 radice \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ costanti radice di D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .

</dd> <dt>

**\_Costanti CD3DX12 radice \_ (uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Crea una nuova istanza di una \_ costante CD3DX12 radice \_ , inizializzando i parametri seguenti:

Num32BitValues UINT

ShaderRegister UINT

consenso esplicito UINT registerSpace = 0

</dd> <dt>

**Init inline (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

Num32BitValues UINT

ShaderRegister UINT

consenso esplicito UINT registerSpace = 0

</dd> <dt>

**static inline init (D3D12 \_ radice \_ costanti &ROOTCONSTANTS, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ \_Costanti radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants

Num32BitValues UINT

ShaderRegister UINT

consenso esplicito UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Costanti radice \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





