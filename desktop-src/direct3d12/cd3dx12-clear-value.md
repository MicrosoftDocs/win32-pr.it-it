---
title: Struttura CD3DX12_CLEAR_VALUE (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura di valori non crittografati D3D12 \_ .
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- Struttura CD3DX12_CLEAR_VALUE
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
ms.openlocfilehash: 6b9dc7afc62c6e9a3e229e6f5bdc4287bf4b85a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322281"
---
# <a name="cd3dx12_clear_value-structure"></a>\_Struttura del valore Clear di CD3DX12 \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ valori non crittografati D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .

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

**\_Valore CD3DX12 Clear \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ valore CD3DX12 Clear \_ .

</dd> <dt>

**valore esplicito CD3DX12 \_ Clear \_ (const D3D12 \_ Clear \_ value &o)**
</dt> <dd>

Crea una nuova istanza di un \_ valore CD3DX12 Clear \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ valori non crittografati D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .

</dd> <dt>

**CD3DX12 \_ Clear \_ value ( \_ formato DXGI, const Float color \[ 4 \] )**
</dt> <dd>

Crea una nuova istanza di un \_ valore CD3DX12 Clear \_ , inizializzando i parametri seguenti:

[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Colore FLOAT \[ 4 \]

</dd> <dt>

**\_Valore CD3DX12 Clear \_ (formato DXGI \_ , profondità float, stencil Uint8)**
</dt> <dd>

Crea una nuova istanza di un \_ valore CD3DX12 Clear \_ , inizializzando i parametri seguenti:

[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Profondità FLOAT

Stencil UINT8

</dd> <dt>

**operator const D3D12 \_ Clear \_ value& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Valore D3D12 Clear \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

