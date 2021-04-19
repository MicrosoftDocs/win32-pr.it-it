---
title: Struttura CD3DX12_GPU_DESCRIPTOR_HANDLE (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura di handle descrittore GPU D3D12 \_ .
ms.assetid: 6E405AD6-D370-4B87-849A-C52D64C79BF7
keywords:
- Struttura CD3DX12_GPU_DESCRIPTOR_HANDLE
topic_type:
- apiref
api_name:
- CD3DX12_GPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429d41d401b7d3e928bc4ab76850b36ae41b1e8a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322264"
---
# <a name="cd3dx12_gpu_descriptor_handle-structure"></a>\_Struttura dell' \_ handle descrittore GPU CD3DX12 \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ \_ handle descrittore GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_GPU_DESCRIPTOR_HANDLE  : public D3D12_GPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            inline operator==( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  bool                            inline operator!=( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_GPU_DESCRIPTOR_HANDLE & operator=(const D3D12_GPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_ \_ Handle descrittore GPU CD3DX12 \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ \_ handle descrittore della GPU CD3DX12 \_ .

</dd> <dt>

**\_ \_ handle descrittore GPU CD3DX12 esplicito \_ (const D3D12 \_ GPU \_ handle descrittore \_ &o)**
</dt> <dd>

Crea una nuova istanza di un \_ \_ handle descrittore della GPU CD3DX12 \_ , inizializzato con il contenuto di un'altra struttura dell' [**\_ \_ \_ handle del descrittore**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) della GPU D3D12.

</dd> <dt>

**\_ \_ Handle descrittore GPU CD3DX12 \_ ( \_ impostazione predefinita CD3DX12)**
</dt> <dd>

Crea una nuova istanza di un \_ \_ handle descrittore della GPU CD3DX12 \_ , inizializzato con parametri predefiniti (imposta il puntatore su zero).

</dd> <dt>

**\_ \_ Handle descrittore GPU CD3DX12 \_ (const D3D12 \_ GPU \_ handle descrittore \_ &other, int offsetScaledByIncrementSize)**
</dt> <dd>

Crea una nuova istanza di un \_ \_ handle descrittore della GPU CD3DX12 \_ , inizializzando i parametri seguenti:

\_ \_ Handle descrittore GPU D3D12 \_ &altro

INT offsetScaledByIncrementSize: numero di incrementi in base a cui eseguire l'offset.

</dd> <dt>

**\_ \_ Handle descrittore GPU CD3DX12 \_ (const D3D12 \_ descrizione della GPU \_ \_ handle &other, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Crea una nuova istanza di un \_ \_ handle descrittore della GPU CD3DX12 \_ , inizializzando i parametri seguenti:

\_ \_ Handle descrittore GPU D3D12 \_ &altro

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

**operatore inline = = ( \_ in \_ const D3D12 \_ GPU \_ descrittore \_ handle& altro) const**
</dt> <dd>

Verifica l'uguaglianza tra l'handle descrittore della GPU CD3DX12 corrente e l'handle descrittore GPU \_ \_ \_ D3D12 specificato \_ o l'handle del \_ \_ \_ \_ descrittore della GPU CD3DX12 \_ .

</dd> <dt>

**operatore inline! = ( \_ in \_ const D3D12 \_ GPU \_ descrittor \_ handle& other) const**
</dt> <dd>

Verifica la disuguaglianza tra l' \_ handle descrittore della GPU CD3DX12 corrente e l'handle descrittore \_ della GPU \_ D3D12 specificato \_ o l'handle del \_ \_ \_ \_ descrittore della GPU CD3DX12 \_ .

</dd> <dt>

**operator = (const D3D12 \_ GPU \_ descrittore \_ handle &altro)**
</dt> <dd>

Imposta l'handle descrittore della GPU CD3DX12 corrente sugli stessi valori dell'handle del descrittore della GPU \_ \_ \_ D3D12 specificato \_ o dell'handle del \_ \_ \_ \_ descrittore della GPU CD3DX12 \_ .

</dd> <dt>

**inline InitOffsetted ( \_ in \_ const D3D12 \_ GPU \_ descrittor \_ handle &base, int offsetScaledByIncrementSize)**
</dt> <dd>

Inizializza una struttura di [**\_ \_ \_ handle del descrittore della GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con il numero specificato di elementi. USA i parametri seguenti:

\_In \_ const D3D12 \_ GPU \_ descrittor \_ handle &base: l'indirizzo di base da cui eseguire l'offset.

INT offsetScaledByIncrementSize: numero di incrementi in base a cui eseguire l'offset.

</dd> <dt>

**inline InitOffsetted ( \_ in \_ const D3D12 \_ GPU \_ descrittor \_ handle &base, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Inizializza una struttura di [**\_ \_ \_ handle del descrittore della GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con un offset, usando il numero specificato di descrittori della dimensione specificata. USA i parametri seguenti:

\_In \_ const D3D12 \_ GPU \_ descrittor \_ handle &base: l'indirizzo di base da cui eseguire l'offset.

INT offsetInDescriptors: numero di descrittori in base a cui eseguire l'offset.

UINT descriptorIncrementSize: valore in base al quale incrementare per ogni descrittore, inclusa la spaziatura interna.

</dd> <dt>

**static inline InitOffsetted ( \_ out \_ D3D12 \_ GPU \_ descrittore handle \_ &handle, \_ in \_ const D3D12 \_ GPU \_ descrittore \_ &base, int offsetScaledByIncrementSize)**
</dt> <dd>

Inizializza una struttura di [**\_ \_ \_ handle del descrittore della GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con un offset, usando il numero specificato di descrittori della dimensione specificata. USA i parametri seguenti:

\_Handle \_ \_ \_ del descrittore D3D12 della gpu in uscita \_ &handle: restituisce l' \_ \_ handle descrittore della GPU D3D12 risultante \_ .

\_In \_ const D3D12 \_ GPU \_ descrittor \_ handle &base: l'indirizzo di base da cui eseguire l'offset.

INT offsetScaledByIncrementSize: numero di incrementi in base a cui eseguire l'offset.

</dd> <dt>

**static inline InitOffsetted ( \_ out \_ D3D12 \_ GPU \_ descrittore handle \_ &handle, \_ in \_ const D3D12 \_ GPU \_ descrittor handle \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Inizializza una struttura di [**\_ \_ \_ handle del descrittore della GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con un offset, usando il numero specificato di descrittori della dimensione specificata. USA i parametri seguenti:

\_Handle \_ \_ \_ del descrittore D3D12 della gpu in uscita \_ &handle: restituisce l' \_ \_ handle descrittore della GPU D3D12 risultante \_ .

\_In \_ const D3D12 \_ GPU \_ descrittor \_ handle &base: l'indirizzo di base da cui eseguire l'offset.

INT offsetInDescriptors: numero di descrittori in base a cui eseguire l'offset.

UINT descriptorIncrementSize: valore in base al quale incrementare per ogni descrittore, inclusa la spaziatura interna.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ \_ Handle descrittore GPU D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





