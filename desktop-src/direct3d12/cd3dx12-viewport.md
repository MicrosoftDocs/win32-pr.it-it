---
title: Struttura CD3DX12_VIEWPORT (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura del viewport D3D12.
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- Struttura CD3DX12_VIEWPORT
topic_type:
- apiref
api_name:
- CD3DX12_VIEWPORT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da29adc50b62bd645070d9667bec1e5c7ce7ab15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323551"
---
# <a name="cd3dx12_viewport-structure"></a>\_Struttura del viewport CD3DX12

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura del [**\_ viewport D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_VIEWPORT  : public D3D12_VIEWPORT{
   CD3DX12_VIEWPORT();
   explicit CD3DX12_VIEWPORT(const D3D12_VIEWPORT& o);
   explicit CD3DX12_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   explicit CD3DX12_VIEWPORT(ID3D12Resource* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   ~CD3DX12_VIEWPORT();
   operator const D3D12_VIEWPORT&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Viewport CD3DX12 ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ viewport CD3DX12.

</dd> <dt>

**Viewport CD3DX12 esplicito \_ (const D3D12 \_ viewport& o)**
</dt> <dd>

Crea una nuova istanza di un \_ viewport CD3DX12, inizializzando i parametri seguenti:

& o del viewport const D3D12 \_

</dd> <dt>

**Viewport CD3DX12 esplicito \_ (float topLeftX, float a sinistra, float width, float height, float minDepth = D3D12 \_ Min \_ Depth, float MaxDepth = D3D12 \_ Max \_ Depth)**
</dt> <dd>

Crea una nuova istanza di un \_ viewport CD3DX12, inizializzando i parametri seguenti:

FLOAT topLeftX

FLOAT a sinistra

Larghezza FLOAT

Altezza FLOAT

FLOAT minDepth = D3D12 \_ Min \_ Depth

FLOAT maxDepth = \_ profondità massima \_ D3D12

</dd> <dt>

**Viewport CD3DX12 esplicito \_ (ID3D12Resource \* PreSource, uint mipSlice = 0, float topLeftX = 0,0 f, float-Lefty = 0,0 f, float MINDEPTH = D3D12 \_ Min \_ Depth, float MaxDepth = D3D12 \_ Max \_ Depth)**
</dt> <dd>

Crea una nuova istanza di un \_ viewport CD3DX12, inizializzando i parametri seguenti:

Preorigine ID3D12Resource \*

UINT mipSlice = 0

FLOAT topLeftX = 0,0 f

FLOAT in uscita = 0,0 f

FLOAT minDepth = D3D12 \_ Min \_ Depth

FLOAT maxDepth = \_ profondità massima \_ D3D12

</dd> <dt>

**Viewport ~ CD3DX12 \_ ()**
</dt> <dd>

Elimina un'istanza di un viewport D3DX12 \_ .

</dd> <dt>

**operatore const D3D12 \_ VIEWPORT& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Viewport D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





