---
title: CD3DX12_RESOURCE_BARRIER struttura (D3dx12.h)
description: Struttura helper per consentire un'inizializzazione semplice di una struttura RESOURCE BARRIER D3D12. \_ \_
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- CD3DX12_RESOURCE_BARRIER struttura
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_BARRIER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3490f48e04c97c845264f514e65db390a01e115ebff7c53aca792d29f0c522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098455"
---
# <a name="cd3dx12_resource_barrier-structure"></a>Struttura CD3DX12 \_ RESOURCE \_ BARRIER

Struttura helper per consentire un'inizializzazione semplice di [**una struttura RESOURCE \_ \_ BARRIER D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_RESOURCE_BARRIER  : public D3D12_RESOURCE_BARRIER{
                           CD3DX12_RESOURCE_BARRIER();
                           explicit CD3DX12_RESOURCE_BARRIER(const D3D12_RESOURCE_BARRIER &o);
  CD3DX12_RESOURCE_BARRIER static inline Transition(ID3D12Resource* pResource, D3D12_RESOURCE_STATES stateBefore, D3D12_RESOURCE_STATES stateAfter, UINT subresource = D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES, D3D12_RESOURCE_BARRIER_FLAGS flags = D3D12_RESOURCE_BARRIER_FLAG_NONE);
  CD3DX12_RESOURCE_BARRIER static inline Aliasing(ID3D12Resource* pResourceBefore, ID3D12Resource* pResourceAfter);
  CD3DX12_RESOURCE_BARRIER static inline UAV(ID3D12Resource* pResource);
                           operator const D3D12_RESOURCE_BARRIER&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ RESOURCE \_ BARRIER()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una barriera di risorse CD3DX12. \_ \_

</dd> <dt>

**explicit CD3DX12 \_ RESOURCE \_ BARRIER(const D3D12 \_ RESOURCE BARRIER &\_ o)**
</dt> <dd>

Crea una nuova istanza di una BARRIERA DI RISORSE CD3DX12, inizializzata con il contenuto di un'altra BARRIERA DI \_ \_ [**\_ RISORSE \_ D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)

</dd> <dt>

**static inline Transition(ID3D12Resource \* pResource, D3D12 \_ RESOURCE \_ STATES stateBefore, D3D12 \_ RESOURCE STATES \_ stateAfter, UINT subresource = D3D12 \_ RESOURCE BARRIER ALL \_ \_ \_ SUBRESOURCES, D3D12 \_ RESOURCE BARRIER FLAGS flags = \_ \_ D3D12 \_ RESOURCE BARRIER FLAG \_ \_ \_ NONE)**
</dt> <dd>

Transizioni tra stati delle risorse, usando i parametri seguenti:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResource

[**D3D12 \_ RESOURCE \_ STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore

[**D3D12 \_ STATO \_ DELLE RISORSEDopo**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)

(scelta esplicita) UiNT subresource = [ **D3D12 \_ RESOURCE \_ BARRIER ALL \_ \_ SUBRESOURCES**](constants.md)

(scelta esplicita) [**D3D12 \_ FLAG \_ DI \_ BARRIERA DELLE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) RISORSE = D3D12 FLAG DI BARRIERA DELLE RISORSE \_ \_ \_ \_ NESSUNO

</dd> <dt>

**aliasing inline statico(ID3D12Resource \* pResourceBefore, ID3D12Resource \* pResourceAfter)**
</dt> <dd>

Crea alias per la risorsa prima e dopo la transizione della barriera. Parametri

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceBefore

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceAfter

</dd> <dt>

**static inline UAV(ID3D12Resource \* pResource)**
</dt> <dd>

Crea una visualizzazione di accesso non ordinato (UAV) per la risorsa. Parametri

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResource

</dd> <dt>

**Operatore const D3D12 \_ RESOURCE \_ BARRIER&() const**
</dt> <dd>

Definisce l& operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BARRIERA DELLE RISORSE D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





