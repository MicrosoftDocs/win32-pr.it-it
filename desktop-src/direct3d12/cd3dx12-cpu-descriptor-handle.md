---
title: CD3DX12_CPU_DESCRIPTOR_HANDLE struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura DESCRIPTOR HANDLE della CPU D3D12. \_ \_ \_
ms.assetid: 91736069-7D13-47B0-B78C-0F6F104F97EB
keywords:
- CD3DX12_CPU_DESCRIPTOR_HANDLE struttura
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
ms.openlocfilehash: c7e6fd6ba75caccf19f3782e0c39581d1e652de0c4187c3c5a203bb5f3b7ceec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913078"
---
# <a name="cd3dx12_cpu_descriptor_handle-structure"></a>Struttura HANDLE DEL \_ DESCRITTORE DELLA CPU CD3DX12 \_ \_

Struttura helper per consentire una facile inizializzazione di [**una struttura \_ \_ DESCRIPTOR \_ HANDLE della CPU D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)

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

**HANDLE DESCRITTORE CPU CD3DX12() \_ \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un HANDLE DESCRITTORE CPU CD3DX12. \_ \_ \_

</dd> <dt>

**HANDLE ESPLICITO DEL DESCRITTORE \_ CPU \_ \_ CD3DX12(const D3D12 \_ CPU \_ DESCRIPTOR HANDLE &\_ o)**
</dt> <dd>

Crea una nuova istanza di un HANDLE DESCRIPTOR CPU CD3DX12, inizializzata con il contenuto di un'altra struttura \_ \_ \_ [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)

</dd> <dt>

**HANDLE DESCRITTORE CPU CD3DX12 (IMPOSTAZIONE PREDEFINITA \_ \_ \_ CD3DX12) \_**
</dt> <dd>

Crea una nuova istanza di un HANDLE DESCRIPTOR CPU CD3DX12, inizializzato con parametri predefiniti \_ \_ \_ (puntatore impostato su zero).

</dd> <dt>

**CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE(const D3D12 \_ CPU \_ DESCRIPTOR HANDLE &\_ other, INT offsetScaledByIncrementSize)**
</dt> <dd>

Crea una nuova istanza di un HANDLE DESCRIPTOR CPU CD3DX12, \_ \_ \_ inizializzando i parametri seguenti:

D3D12 \_ CPU \_ DESCRIPTOR HANDLE &\_ altro

INT offsetScaledByIncrementSize: numero di incrementi di cui eseguire l'offset.

</dd> <dt>

**CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE(const D3D12 \_ CPU \_ DESCRIPTOR HANDLE &\_ other, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Crea una nuova istanza di un HANDLE DESCRIPTOR CPU CD3DX12, \_ \_ \_ inizializzando i parametri seguenti:

D3D12 \_ CPU \_ DESCRIPTOR HANDLE &\_ altro

INT offsetInDescriptors: numero di descrittori di cui eseguire l'incremento.

UINT descriptorIncrementSize: quantità di incremento per ogni descrittore, inclusa la spaziatura interna.

</dd> <dt>

**Offset(INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Imposta l'offset in base al numero specificato di descrittori e alla quantità da incrementare per ogni descrittore. Usa i parametri seguenti:

INT offsetInDescriptors: numero di descrittori di cui eseguire l'incremento.

UINT descriptorIncrementSize: quantità di incremento per ogni descrittore, inclusa la spaziatura interna.

</dd> <dt>

**Offset(INT offsetScaledByIncrementSize)**
</dt> <dd>

Imposta l'offset in base al numero specificato di incrementi. Usa i parametri seguenti:

INT offsetScaledByIncrementSize: numero di incrementi di cui eseguire l'offset.

</dd> <dt>

**operator==( \_ In \_ const D3D12 \_ CPU \_ DESCRIPTOR HANDLE& \_ other) const**
</dt> <dd>

Verifica l'uguaglianza tra l'HANDLE DESCRIPTOR CPU CD3DX12 corrente e l'HANDLE descrittore CPU \_ \_ \_ D3D12 specificato o \_ \_ \_ CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE.

</dd> <dt>

**operator!=( \_ In \_ const D3D12 \_ CPU \_ DESCRIPTOR HANDLE& \_ other) const**
</dt> <dd>

Verifica la disuguaglianza tra l'handle del DESCRITTOre CPU CD3DX12 corrente e l'HANDLE descrittore CPU \_ \_ \_ D3D12 specificato o \_ \_ \_ CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE.

</dd> <dt>

**operator=(const D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &other)**
</dt> <dd>

Imposta l'handle del DESCRITTOre CPU CD3DX12 corrente sullo stesso valore dell'handle del DESCRITTOre CPU \_ \_ \_ D3D12 o \_ \_ \_ CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE specificato.

</dd> <dt>

**inline InitOffsetted( \_ In \_ const D3D12 \_ CPU \_ DESCRIPTOR HANDLE &\_ base, INT offsetScaledByIncrementSize)**
</dt> <dd>

Inizializza una struttura [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con il numero specificato di elementi. Usa i parametri seguenti:

\_In \_ const D3D12 \_ CPU \_ DESCRIPTOR HANDLE &base: indirizzo di base da cui eseguire \_ l'offset.

INT offsetScaledByIncrementSize: numero di incrementi di cui eseguire l'offset.

</dd> <dt>

**inline InitOffsetted( \_ In \_ const D3D12 \_ CPU \_ DESCRIPTOR HANDLE &\_ base, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Inizializza una struttura [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un offset, usando il numero specificato di descrittori delle dimensioni specificate. Usa i parametri seguenti:

\_In \_ const D3D12 \_ CPU \_ DESCRIPTOR HANDLE &base: indirizzo di base da cui eseguire \_ l'offset.

INT offsetInDescriptors: numero di descrittori in base al quale eseguire l'offset.

UINT descriptorIncrementSize: quantità di incremento per ogni descrittore, inclusa la spaziatura interna.

</dd> <dt>

**static inline InitOffsetted( \_ Out \_ D3D12 \_ CPU \_ DESCRIPTOR HANDLE &\_ handle, In \_ \_ const D3D12 \_ CPU \_ DESCRIPTOR HANDLE &\_ base, INT offsetScaledByIncrementSize)**
</dt> <dd>

Inizializza una struttura [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un offset, usando il numero specificato di descrittori delle dimensioni specificate. Usa i parametri seguenti:

\_Out \_ D3D12 \_ CPU DESCRIPTOR HANDLE &handle: restituisce l'handle del DESCRITTOre CPU \_ \_ D3D12 \_ \_ \_ risultante.

\_In \_ const D3D12 \_ CPU \_ DESCRIPTOR HANDLE &base: indirizzo di base da cui eseguire \_ l'offset.

INT offsetScaledByIncrementSize: numero di incrementi di cui eseguire l'offset.

</dd> <dt>

**static inline InitOffsetted( \_ Out \_ D3D12 \_ CPU \_ DESCRIPTOR HANDLE &\_ handle, In \_ \_ const D3D12 \_ CPU \_ DESCRIPTOR HANDLE &\_ base, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Inizializza una struttura [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un offset, usando il numero specificato di descrittori delle dimensioni specificate. Usa i parametri seguenti:

\_Out \_ D3D12 \_ CPU DESCRIPTOR HANDLE &handle: restituisce l'handle del DESCRITTOre CPU \_ \_ D3D12 \_ \_ \_ risultante.

\_In \_ const D3D12 \_ CPU \_ DESCRIPTOR HANDLE &base: indirizzo di base da cui eseguire \_ l'offset.

INT offsetInDescriptors: numero di descrittori in base al quale eseguire l'offset.

UINT descriptorIncrementSize: quantità di incremento per ogni descrittore, inclusa la spaziatura interna.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





