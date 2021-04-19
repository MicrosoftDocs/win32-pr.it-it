---
title: Struttura CD3DX12_ROOT_DESCRIPTOR (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di \_ una \_ struttura del descrittore radice D3D12.
ms.assetid: DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC
keywords:
- Struttura CD3DX12_ROOT_DESCRIPTOR
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710064436e0287b570700ff5812b728ca62be56d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323562"
---
# <a name="cd3dx12_root_descriptor-structure"></a>\_Struttura del \_ descrittore radice CD3DX12

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura del [**\_ \_ descrittore radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_ROOT_DESCRIPTOR  : public D3D12_ROOT_DESCRIPTOR{
       CD3DX12_ROOT_DESCRIPTOR();
       explicit CD3DX12_ROOT_DESCRIPTOR(const D3D12_ROOT_DESCRIPTOR &o);
       CD3DX12_ROOT_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Descrittore radice CD3DX12 \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ \_ descrittore radice CD3DX12.

</dd> <dt>

**descrittore radice CD3DX12 esplicito \_ \_ ( \_ descrittore radice D3D12 const \_ &o)**
</dt> <dd>

Crea una nuova istanza di un \_ \_ descrittore radice CD3DX12, inizializzato con il contenuto di un'altra struttura del [**\_ \_ descrittore radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .

</dd> <dt>

**\_Descrittore radice CD3DX12 \_ (uint SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Crea una nuova istanza di un \_ \_ descrittore radice CD3DX12, inizializzando i parametri seguenti:

ShaderRegister UINT

consenso esplicito UINT registerSpace = 0

</dd> <dt>

**Init inline (UINT shaderRegister, UINT registerSpace = 0)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

ShaderRegister UINT

consenso esplicito UINT registerSpace = 0

</dd> <dt>

**static inline init (D3D12 \_ radice \_ descrittore &tabella, uint SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ \_Descrittore radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) &tabella

ShaderRegister UINT

consenso esplicito UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Descrittore radice D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





