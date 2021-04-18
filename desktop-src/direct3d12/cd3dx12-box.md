---
title: Struttura CD3DX12_BOX (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di D3D12 \_ box.
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- Struttura CD3DX12_BOX
topic_type:
- apiref
api_name:
- CD3DX12_BOX
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.topic: reference
ms.localizationpriority: low
ms.date: 05/31/2018
ms.openlocfilehash: c689c9bfe611651248280f7536bd91a9f4d003d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322282"
---
# <a name="cd3dx12_box-structure"></a>\_Struttura CD3DX12 box

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**D3D12 \_ Box**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_BOX  : public D3D12_BOX{
   CD3DX12_BOX();
   explicit CD3DX12_BOX(const D3D12_BOX& o);
   explicit CD3DX12_BOX(LONG Left, LONG Right);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back);
   ~CD3DX12_BOX();
   operator const D3D12_BOX&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ Box ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ casella CD3DX12.

</dd> <dt>

**casella CD3DX12 esplicita \_ (const D3D12 \_ Box& o)**
</dt> <dd>

Crea una nuova istanza di una \_ casella CD3DX12, inizializzata con il contenuto di un'altra struttura di [**\_ caselle di D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .

</dd> <dt>

**casella CD3DX12 esplicita \_ (Long Left, Long Right)**
</dt> <dd>

Crea una nuova istanza di una \_ casella CD3DX12, inizializzando i parametri seguenti:

LONG Left

LUNGO a destra

</dd> <dt>

**casella CD3DX12 esplicita \_ (Long Left, Long Top, Long Right, Long Bottom)**
</dt> <dd>

Crea una nuova istanza di una \_ casella CD3DX12, inizializzando i parametri seguenti:

LONG Left

Inizio lungo

LUNGO a destra

LUNGO in basso

</dd> <dt>

**casella CD3DX12 esplicita \_ (Long Left, Long Top, Long Front, Long Right, Long Bottom, Long back)**
</dt> <dd>

Crea una nuova istanza di una \_ casella CD3DX12, inizializzando i parametri seguenti:

LONG Left

Inizio lungo

LUNGO Front

LUNGO a destra

LUNGO in basso

LONG back

</dd> <dt>

**~ CD3DX12 \_ Box ()**
</dt> <dd>

Elimina un'istanza di una casella CD3DX12 \_ .

</dd> <dt>

**operatore const D3D12 \_ BOX& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Casella D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





