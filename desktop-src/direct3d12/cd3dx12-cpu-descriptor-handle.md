---
title: Struttura CD3DX12_CPU_DESCRIPTOR_HANDLE (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di \_ una \_ struttura di handle del descrittore della CPU D3D12 \_ .
ms.assetid: 91736069-7D13-47B0-B78C-0F6F104F97EB
keywords:
- Struttura CD3DX12_CPU_DESCRIPTOR_HANDLE
topic_type:
- apiref
api_name:
- CD3DX12_CPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1045202c531aa200745fc89ed067628a175486
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322280"
---
# <a name="cd3dx12_cpu_descriptor_handle-structure"></a>\_Struttura dell' \_ handle del descrittore della CPU CD3DX12 \_

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ \_ handle del descrittore della CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_CPU_DESCRIPTOR_HANDLE  : public D3D12_CPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            operator==( _In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  bool                            operator!=(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_CPU_DESCRIPTOR_HANDLE & operator=(const D3D12_CPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_ \_ Handle descrittore CPU CD3DX12 \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ \_ handle del descrittore della CPU CD3DX12 \_ .

</dd> <dt>

**handle del \_ descrittore della CPU CD3DX12 esplicito \_ \_ (const D3D12 \_ CPU \_ \_ handle &o)**
</dt> <dd>

Crea una nuova istanza di un \_ \_ handle descrittore della CPU CD3DX12 \_ , inizializzato con il contenuto di un'altra struttura dell' [**\_ \_ \_ handle del descrittore della CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .

</dd> <dt>

**\_ \_ Handle descrittore CPU CD3DX12 \_ ( \_ impostazione predefinita CD3DX12)**
</dt> <dd>

Crea una nuova istanza di un \_ \_ handle descrittore della CPU CD3DX12 \_ , inizializzato con parametri predefiniti (puntatore impostato su zero).

</dd> <dt>

**\_ \_ Handle descrittore CPU CD3DX12 \_ (const D3D12 \_ CPU \_ descrittore \_ handle &other, int offsetScaledByIncrementSize)**
</dt> <dd>

Crea una nuova istanza di un \_ \_ handle descrittore della CPU CD3DX12 \_ , inizializzando i parametri seguenti:

\_ \_ Handle descrittore CPU D3D12 \_ &altro

INT offsetScaledByIncrementSize: numero di incrementi in base a cui eseguire l'offset.

</dd> <dt>

**\_ \_ Handle descrittore CPU CD3DX12 \_ (const D3D12 \_ CPU \_ descrittore \_ handle &other, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Crea una nuova istanza di un \_ \_ handle descrittore della CPU CD3DX12 \_ , inizializzando i parametri seguenti:

\_ \_ Handle descrittore CPU D3D12 \_ &altro

INT offsetInDescriptors: numero di descrittori in base a cui incrementare.

UINT descriptorIncrementSize: valore in base al quale incrementare per ogni descrittore, inclusa la spaziatura interna.

</dd> <dt>

**Offset (INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Imposta l'offset in base al numero specificato di descrittori e alla quantità di incremento per ogni descrittore. USA i parametri seguenti:

INT offsetInDescriptors: numero di descrittori in base a cui incrementare.

UINT descriptorIncrementSize: valore in base al quale incrementare per ogni descrittore, inclusa la spaziatura interna.

</dd> <dt>

**Offset (INT offsetScaledByIncrementSize)**
</dt> <dd>

Imposta l'offset in base al numero di incrementi specificato. USA i parametri seguenti:

INT offsetScaledByIncrementSize: numero di incrementi in base a cui eseguire l'offset.

</dd> <dt>

**operator = = ( \_ in \_ const D3D12 \_ CPU \_ descrittore \_ handle& altro) const**
</dt> <dd>

Verifica l'uguaglianza tra l'handle descrittore della CPU CD3DX12 corrente e l'handle descrittore della CPU \_ \_ \_ D3D12 specificato \_ \_ o l' \_ \_ \_ handle del descrittore della CPU CD3DX12 \_

</dd> <dt>

**operator! = ( \_ in \_ const D3D12 \_ CPU \_ descrittore \_ handle& altro) const**
</dt> <dd>

Verifica la disuguaglianza tra l'handle descrittore della CPU CD3DX12 corrente e l'handle del descrittore della CPU \_ \_ \_ D3D12 specificato \_ o l'handle del \_ \_ \_ \_ descrittore della CPU CD3DX12 \_ .

</dd> <dt>

**operator = (const D3D12 \_ CPU \_ descrittore \_ handle &altro)**
</dt> <dd>

Imposta l'handle del descrittore della CPU CD3DX12 corrente sugli stessi valori dell'handle del descrittore della CPU \_ \_ \_ D3D12 specificato \_ o dell'handle del \_ \_ \_ \_ descrittore della CPU CD3DX12 \_ .

</dd> <dt>

**inline InitOffsetted ( \_ in \_ const D3D12 \_ CPU \_ descrittore \_ handle &base, int offsetScaledByIncrementSize)**
</dt> <dd>

Inizializza una struttura di [**\_ \_ \_ handle del descrittore della CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con il numero specificato di elementi. USA i parametri seguenti:

\_In \_ const D3D12 \_ CPU \_ descrittor \_ handle &base: l'indirizzo di base da cui eseguire l'offset.

INT offsetScaledByIncrementSize: numero di incrementi in base a cui eseguire l'offset.

</dd> <dt>

**inline InitOffsetted ( \_ in \_ const D3D12 \_ CPU \_ descrittore \_ handle &base, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Inizializza una struttura di [**\_ \_ \_ handle del descrittore della CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un offset, usando il numero specificato di descrittori della dimensione specificata. USA i parametri seguenti:

\_In \_ const D3D12 \_ CPU \_ descrittor \_ handle &base: l'indirizzo di base da cui eseguire l'offset.

INT offsetInDescriptors: numero di descrittori in base a cui eseguire l'offset.

UINT descriptorIncrementSize: valore in base al quale incrementare per ogni descrittore, inclusa la spaziatura interna.

</dd> <dt>

**static inline InitOffsetted ( \_ out \_ D3D12 \_ CPU \_ descrittore handle \_ &handle, \_ in \_ const D3D12 \_ CPU \_ descrittore handle \_ &base, int offsetScaledByIncrementSize)**
</dt> <dd>

Inizializza una struttura di [**\_ \_ \_ handle del descrittore della CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un offset, usando il numero specificato di descrittori della dimensione specificata. USA i parametri seguenti:

\_Handle \_ \_ \_ del descrittore della cpu out D3D12 &handle \_ : restituisce l' \_ \_ handle descrittore della CPU D3D12 risultante \_ .

\_In \_ const D3D12 \_ CPU \_ descrittor \_ handle &base: l'indirizzo di base da cui eseguire l'offset.

INT offsetScaledByIncrementSize: numero di incrementi in base a cui eseguire l'offset.

</dd> <dt>

**static inline InitOffsetted ( \_ out \_ D3D12 \_ CPU \_ descrittore handle \_ &handle, \_ in \_ const D3D12 \_ CPU \_ descrittore handle \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Inizializza una struttura di [**\_ \_ \_ handle del descrittore della CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un offset, usando il numero specificato di descrittori della dimensione specificata. USA i parametri seguenti:

\_Handle \_ \_ \_ del descrittore della cpu out D3D12 &handle \_ : restituisce l' \_ \_ handle descrittore della CPU D3D12 risultante \_ .

\_In \_ const D3D12 \_ CPU \_ descrittor \_ handle &base: l'indirizzo di base da cui eseguire l'offset.

INT offsetInDescriptors: numero di descrittori in base a cui eseguire l'offset.

UINT descriptorIncrementSize: valore in base al quale incrementare per ogni descrittore, inclusa la spaziatura interna.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





