---
title: CD3DX12_RECT struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura D3D12 \_ RECT.
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- CD3DX12_RECT struttura
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
ms.openlocfilehash: bff9df3a4c7df2f30e9614b16d5f8b89ea1b6f0279a1566b206cabef7260fb28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729341"
---
# <a name="cd3dx12_rect-structure"></a>Struttura RECT CD3DX12 \_

Struttura helper per consentire una facile inizializzazione di [**una struttura D3D12 \_ RECT.**](d3d12-rect.md)

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

**CD3DX12 \_ RECT()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un oggetto CD3DX12 \_ RECT.

</dd> <dt>

**EXPLICIT CD3DX12 \_ RECT(const D3D12 \_ RECT& o)**
</dt> <dd>

Crea una nuova istanza di un oggetto CD3DX12 RECT, inizializzato con il contenuto di \_ [**un'altra struttura RECT D3D12. \_**](d3d12-rect.md)

</dd> <dt>

**EXPLICIT CD3DX12 \_ RECT(LONG Left, LONG Top, LONG Right, LONG Bottom)**
</dt> <dd>

Crea una nuova istanza di un oggetto CD3DX12 \_ RECT, inizializzando i parametri seguenti:

LONG A sinistra

LONG Top

LONG Right

LONG In basso

</dd> <dt>

**~CD3DX12 \_ RECT()**
</dt> <dd>

Elimina un'istanza di un oggetto CD3DX12 \_ RECT.

</dd> <dt>

**operator const D3D12 \_ RECT&() const**
</dt> <dd>

Definisce l'& operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ RECT**](d3d12-rect.md)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





