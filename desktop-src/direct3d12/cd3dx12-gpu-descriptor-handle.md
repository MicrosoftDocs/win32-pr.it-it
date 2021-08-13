---
title: CD3DX12_GPU_DESCRIPTOR_HANDLE struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura DESCRIPTOR HANDLE della GPU D3D12. \_ \_ \_
ms.assetid: 6E405AD6-D370-4B87-849A-C52D64C79BF7
keywords:
- CD3DX12_GPU_DESCRIPTOR_HANDLE struttura
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
ms.openlocfilehash: d8039b20be8898c7bc81e57926ab82cd662d9e8a702d2d7a720915a1e35bcc93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461001"
---
# <a name="cd3dx12_gpu_descriptor_handle-structure"></a>Struttura \_ \_ DESCRIPTOR HANDLE CD3DX12 GPU \_

Struttura helper per consentire una facile inizializzazione di una [**struttura \_ \_ DESCRIPTOR \_ HANDLE della GPU D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)

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

**CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un HANDLE DESCRITTORE GPU CD3DX12. \_ \_ \_

</dd> <dt>

**HANDLE descrittore GPU CD3DX12 \_ \_ \_ esplicito(const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &o)**
</dt> <dd>

Crea una nuova istanza di un HANDLE DESCRIPTOR CD3DX12 GPU, inizializzato con il contenuto di un'altra struttura \_ \_ \_ [**\_ \_ DESCRIPTOR \_ HANDLE della GPU D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)

</dd> <dt>

**HANDLE DESCRITTORE GPU CD3DX12 (IMPOSTAZIONE PREDEFINITA \_ \_ \_ CD3DX12) \_**
</dt> <dd>

Crea una nuova istanza di un HANDLE DESCRIPTOR CD3DX12 GPU, inizializzato con parametri predefiniti \_ \_ \_ (imposta il puntatore su zero).

</dd> <dt>

**CD3DX12 \_ \_ GPU DESCRIPTOR \_ HANDLE(const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &other, INT offsetScaledByIncrementSize)**
</dt> <dd>

Crea una nuova istanza di UN HANDLE DESCRITTORE \_ GPU CD3DX12, \_ \_ inizializzando i parametri seguenti:

D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &altro

INT offsetScaledByIncrementSize: numero di incrementi di cui eseguire l'offset.

</dd> <dt>

**CD3DX12 \_ \_ GPU DESCRIPTOR \_ HANDLE(const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Crea una nuova istanza di UN HANDLE DESCRITTORE \_ GPU CD3DX12, \_ \_ inizializzando i parametri seguenti:

D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &altro

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

**inline operator==( \_ In \_ const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE& other) const**
</dt> <dd>

Verifica l'uguaglianza tra l'handle del descrittore GPU CD3DX12 corrente e l'HANDLE descrittore \_ \_ \_ GPU D3D12 specificato o \_ \_ \_ CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE.

</dd> <dt>

**operatore inline!=( \_ In \_ const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE& other) const**
</dt> <dd>

Verifica la disuguaglianza tra l'handle del descrittore GPU CD3DX12 corrente e l'HANDLE descrittore \_ \_ \_ GPU D3D12 specificato o \_ \_ \_ CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE.

</dd> <dt>

**operator=(const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &other)**
</dt> <dd>

Imposta l'handle del DESCRITTOre GPU CD3DX12 corrente sullo stesso valore dell'HANDLE descrittore \_ \_ \_ GPU D3D12 o \_ \_ \_ CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE specificato.

</dd> <dt>

**inline InitOffsetted( \_ In \_ const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &base, INT offsetScaledByIncrementSize)**
</dt> <dd>

Inizializza una struttura [**\_ \_ DESCRIPTOR \_ HANDLE della GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con il numero specificato di elementi. Usa i parametri seguenti:

\_In \_ const D3D12 \_ GPU DESCRIPTOR HANDLE &base: indirizzo di base da cui eseguire \_ \_ l'offset.

INT offsetScaledByIncrementSize: numero di incrementi di cui eseguire l'offset.

</dd> <dt>

**inline InitOffsetted( \_ In \_ const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Inizializza una [**struttura \_ \_ DESCRIPTOR \_ HANDLE della GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con un offset, usando il numero specificato di descrittori delle dimensioni specificate. Usa i parametri seguenti:

\_In \_ const D3D12 \_ GPU DESCRIPTOR HANDLE &base: indirizzo di base da cui eseguire \_ \_ l'offset.

INT offsetInDescriptors: numero di descrittori in base al quale eseguire l'offset.

UINT descriptorIncrementSize: quantità di incremento per ogni descrittore, inclusa la spaziatura interna.

</dd> <dt>

**static inline InitOffsetted( \_ Out \_ D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &handle, In \_ \_ const D3D12 \_ GPU \_ DESCRIPTOR HANDLE &\_ base, INT offsetScaledByIncrementSize)**
</dt> <dd>

Inizializza una [**struttura \_ \_ DESCRIPTOR \_ HANDLE della GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con un offset, usando il numero specificato di descrittori delle dimensioni specificate. Usa i parametri seguenti:

\_Out \_ D3D12 \_ GPU \_ DESCRIPTOR HANDLE &handle: restituisce l'handle del descrittore \_ GPU D3D12 \_ \_ \_ risultante.

\_In \_ const D3D12 \_ GPU DESCRIPTOR HANDLE &base: indirizzo di base da cui eseguire \_ \_ l'offset.

INT offsetScaledByIncrementSize: numero di incrementi di cui eseguire l'offset.

</dd> <dt>

**static inline InitOffsetted( \_ Out \_ D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &handle, In \_ \_ const D3D12 \_ GPU \_ DESCRIPTOR HANDLE &\_ base, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Inizializza una [**struttura \_ \_ DESCRIPTOR \_ HANDLE della GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con un offset, usando il numero specificato di descrittori delle dimensioni specificate. Usa i parametri seguenti:

\_Out \_ D3D12 \_ GPU \_ DESCRIPTOR HANDLE &handle: restituisce l'handle del descrittore \_ GPU D3D12 \_ \_ \_ risultante.

\_In \_ const D3D12 \_ GPU DESCRIPTOR HANDLE &base: indirizzo di base da cui eseguire \_ \_ l'offset.

INT offsetInDescriptors: numero di descrittori in base al quale eseguire l'offset.

UINT descriptorIncrementSize: quantità di incremento per ogni descrittore, inclusa la spaziatura interna.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**HANDLE DESCRITTORE GPU D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





