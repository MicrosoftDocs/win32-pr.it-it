---
title: Struttura CD3DX12_RESOURCE_BARRIER (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura di barriera delle risorse D3D12 \_ .
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- Struttura CD3DX12_RESOURCE_BARRIER
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
ms.openlocfilehash: 8eaa9b19a8bc7dcebba5982313bb362dbcee6157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323568"
---
# <a name="cd3dx12_resource_barrier-structure"></a>\_Struttura della barriera delle risorse CD3DX12 \_

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ barriera delle risorse D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) .

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

**\_Barriera risorse CD3DX12 \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ barriera della risorsa CD3DX12 \_ .

</dd> <dt>

**barriera della risorsa CD3DX12 esplicita \_ \_ (const D3D12 \_ Resource \_ Barrier &o)**
</dt> <dd>

Crea una nuova istanza di una \_ barriera della risorsa CD3DX12 \_ , inizializzata con il contenuto di un'altra [**\_ \_ barriera di risorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).

</dd> <dt>

**transizione inline statica ( \* preorigine ID3D12Resource, \_ Stati risorsa D3D12 \_ stateBefore, D3D12 \_ \_ stati risorse stateAfter, uint subresource = D3D12 \_ Resource \_ Barrier \_ All \_ Resources, D3D12 Resource Barrier flag Flags \_ \_ \_ = D3D12 \_ Resource \_ Barrier \_ flag \_ None)**
</dt> <dd>

Transizioni tra gli Stati delle risorse, usando i parametri seguenti:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResource

[**D3D12 \_ \_Stati delle risorse**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore

[**D3D12 \_ \_Stati delle risorse**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter

consenso esplicito UINT subresource = [ **D3D12 \_ Resource \_ Barrier \_ tutte le \_ sottorisorse**](constants.md)

consenso esplicito [**D3D12 \_ Flag \_ di \_ barriera delle risorse**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) flag = D3D12 \_ flag di barriera delle risorse \_ \_ \_ None

</dd> <dt>

**Aliasing inline statico (ID3D12Resource \* pResourceBefore, ID3D12Resource \* pResourceAfter)**
</dt> <dd>

Crea gli alias per la risorsa prima e dopo la transizione della barriera. Parametri

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceBefore

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceAfter

</dd> <dt>

**inline UAV statico ( \* preorigine ID3D12Resource)**
</dt> <dd>

Crea una visualizzazione non ordinata (UAV) per la risorsa. Parametri

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResource

</dd> <dt>

**operatore const D3D12 \_ Resource \_ Barrier& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Barriera delle risorse D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





