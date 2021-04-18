---
title: Struttura CD3DX12_RECT (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura Rect D3D12.
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- Struttura CD3DX12_RECT
topic_type:
- apiref
api_name:
- CD3DX12_RECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d8c133f14b531433ceb2239377ea85ba212af
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322217"
---
# <a name="cd3dx12_rect-structure"></a>\_Struttura Rect CD3DX12

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura [**\_ Rect D3D12**](d3d12-rect.md) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_RECT  : public D3D12_RECT{
   CD3DX12_RECT();
   explicit CD3DX12_RECT(const D3D12_RECT& o);
   explicit CD3DX12_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom);
   ~CD3DX12_RECT();
   operator const D3D12_RECT&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ Rect ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ rettangolo CD3DX12.

</dd> <dt>

**Explicit CD3DX12 \_ Rect (const D3D12 \_ Rect& o)**
</dt> <dd>

Crea una nuova istanza di un oggetto CD3DX12 \_ Rect, inizializzato con il contenuto di un'altra struttura [**\_ Rect di D3D12**](d3d12-rect.md) .

</dd> <dt>

**Rect CD3DX12 esplicito \_ (Long Left, Long Top, Long Right, Long Bottom)**
</dt> <dd>

Crea una nuova istanza di un oggetto CD3DX12 \_ Rect, inizializzando i parametri seguenti:

LONG Left

Inizio lungo

LUNGO a destra

LUNGO in basso

</dd> <dt>

**~ CD3DX12 \_ Rect ()**
</dt> <dd>

Elimina un'istanza di un CD3DX12 \_ Rect.

</dd> <dt>

**operatore const D3D12 \_ RECT& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ Rect**](d3d12-rect.md)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





