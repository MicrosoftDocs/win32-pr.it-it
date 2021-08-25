---
title: CD3DX12_CLEAR_VALUE struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura D3D12 \_ CLEAR \_ VALUE.
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- CD3DX12_CLEAR_VALUE struttura
topic_type:
- apiref
api_name:
- CD3DX12_CLEAR_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785ab3c8312949bfc692fcd7c8d1dace28734ce08e5763387a744eb28f2000f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988491"
---
# <a name="cd3dx12_clear_value-structure"></a>Struttura CD3DX12 \_ CLEAR \_ VALUE

Struttura helper per consentire una facile inizializzazione di [**una struttura CLEAR \_ \_ VALUE D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_CLEAR_VALUE  : public D3D12_CLEAR_VALUE{
   CD3DX12_CLEAR_VALUE();
   explicit CD3DX12_CLEAR_VALUE(const D3D12_CLEAR_VALUE &o);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, const FLOAT color[ 4 ]);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, FLOAT depth, UINT8 stencil);
   operator const D3D12_CLEAR_VALUE&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ CLEAR \_ VALUE()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un VALORE CLEAR CD3DX12. \_ \_

</dd> <dt>

**EXPLICIT CD3DX12 \_ CLEAR \_ VALUE(const D3D12 \_ CLEAR VALUE &\_ o)**
</dt> <dd>

Crea una nuova istanza di un VALORE CLEAR CD3DX12, inizializzato con il contenuto di \_ \_ un'altra struttura [**D3D12 \_ CLEAR \_ VALUE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)

</dd> <dt>

**CD3DX12 \_ CLEAR \_ VALUE(formato DXGI, \_ const FLOAT color \[ 4 \] )**
</dt> <dd>

Crea una nuova istanza di UN VALORE CLEAR CD3DX12, \_ \_ inizializzando i parametri seguenti:

[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Colore FLOAT \[ 4 \]

</dd> <dt>

**CD3DX12 \_ CLEAR \_ VALUE (formato DXGI, \_ profondità FLOAT, stencil UINT8)**
</dt> <dd>

Crea una nuova istanza di UN VALORE CLEAR CD3DX12, \_ \_ inizializzando i parametri seguenti:

[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Profondità FLOAT

Stencil UINT8

</dd> <dt>

**operator const D3D12 \_ CLEAR \_ VALUE&() const**
</dt> <dd>

Definisce l'& operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**VALORE DI CANCELLAZIONE D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

