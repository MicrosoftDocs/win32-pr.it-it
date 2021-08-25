---
title: CD3DX12_BOX struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura D3D12 \_ BOX.
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- CD3DX12_BOX struttura
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
ms.openlocfilehash: f2aa358d8b2d772d45c6387221dd9e660a9630fbf90535ada7dcceefc3257879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851411"
---
# <a name="cd3dx12_box-structure"></a>Struttura CD3DX12 \_ BOX

Struttura helper per consentire una facile inizializzazione di [**una struttura D3D12 \_ BOX.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)

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

**CD3DX12 \_ BOX()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un OGGETTO CD3DX12 \_ BOX.

</dd> <dt>

**EXPLICIT CD3DX12 \_ BOX(const D3D12 \_ BOX& o)**
</dt> <dd>

Crea una nuova istanza di cd3DX12 BOX, inizializzata con il contenuto di \_ [**un'altra struttura D3D12 \_ BOX.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)

</dd> <dt>

**EXPLICIT CD3DX12 \_ BOX(LONG Left, LONG Right)**
</dt> <dd>

Crea una nuova istanza di cd3DX12 \_ BOX, inizializzando i parametri seguenti:

LONG A sinistra

LONG Right

</dd> <dt>

**EXPLICIT CD3DX12 \_ BOX(LONG Left, LONG Top, LONG Right, LONG Bottom)**
</dt> <dd>

Crea una nuova istanza di cd3DX12 \_ BOX, inizializzando i parametri seguenti:

LONG A sinistra

LONG Top

LONG Right

LONG In basso

</dd> <dt>

**EXPLICIT CD3DX12 \_ BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back)**
</dt> <dd>

Crea una nuova istanza di cd3DX12 \_ BOX, inizializzando i parametri seguenti:

LONG A sinistra

LONG Top

LONG Front

LONG Right

LONG In basso

LONG Back

</dd> <dt>

**~CD3DX12 \_ BOX()**
</dt> <dd>

Elimina un'istanza di cd3DX12 \_ BOX.

</dd> <dt>

**operator const D3D12 \_ BOX&() const**
</dt> <dd>

Definisce l'& operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





