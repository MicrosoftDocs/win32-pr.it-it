---
title: Struttura CD3DX12_RANGE (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura di intervallo D3D12.
ms.assetid: 5D5192BF-D14C-487B-A214-F8428E82AF0E
keywords:
- Struttura CD3DX12_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b6b92cd24a981d48252f5ad457f7ac0320e2d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323570"
---
# <a name="cd3dx12_range-structure"></a>\_Struttura dell'intervallo CD3DX12

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ intervallo D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_RANGE  : public D3D12_RANGE{
   CD3DX12_RANGE();
   explicit CD3DX12_RANGE(const D3D12_RANGE &o);
   CD3DX12_RANGE(SIZE_T begin, SIZE_T end);
   operator const D3D12_RANGE&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Intervallo CD3DX12 ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un intervallo di CD3DX12 \_ .

</dd> <dt>

**intervallo CD3DX12 esplicito \_ (const D3D12 \_ Range &o)**
</dt> <dd>

Crea una nuova istanza di un intervallo di CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura di [**\_ intervallo D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .

</dd> <dt>

**\_Intervallo CD3DX12 (size \_ t begin, Size \_ t end)**
</dt> <dd>

Crea una nuova istanza di un intervallo di CD3DX12 \_ , inizializzando i parametri seguenti:

DIMENSIONI \_ T Begin

DIMENSIONI \_ T End

</dd> <dt>

**operatore const D3D12 \_ RANGE& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Intervallo D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





