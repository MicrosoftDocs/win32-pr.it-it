---
title: Struttura CD3DX12_RT_FORMAT_ARRAY (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di \_ una \_ struttura di matrici di formato D3D12 RT \_ .
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- Struttura CD3DX12_RT_FORMAT_ARRAY
topic_type:
- apiref
api_name:
- CD3DX12_RT_FORMAT_ARRAY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05b7ae9e51d2d6b2a43f45dc83bda2074f6b734
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323553"
---
# <a name="cd3dx12_rt_format_array-structure"></a>\_Struttura della \_ matrice di formato CD3DX12 RT \_

Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ matrici di \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ RT \_ Format \_ Array ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ matrice di formato CD3DX12 \_ RT \_ .

</dd> <dt>

**matrice di \_ formato CD3DX12 RT esplicita \_ \_ (const D3D12 \_ RT \_ Format \_ Array& o)**
</dt> <dd>

Crea una nuova istanza di una \_ matrice di formato CD3DX12 RT \_ \_ , inizializzata con i valori copiati da una struttura di [**\_ \_ \_ matrice di formato D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

</dd> <dt>

**matrice di \_ formato CD3DX12 RT esplicita \_ \_ (const DXGI \_ Format \* pFormats, uint NumFormats)**
</dt> <dd>

Crea una nuova istanza di una \_ matrice di formato CD3DX12 RT \_ \_ , inizializzata con i valori passati nell'elenco di parametri. Il contenuto della matrice specificata dal parametro *pFormats* viene copiato nella matrice membro **RTFormats**. Si presuppone che la matrice specificata da *pFormats* abbia le stesse dimensioni di **RTFormats**.

</dd> <dt>

**operatore const D3D12 \_ RT \_ FORMAT \_ Array& () const**
</dt> <dd>

Conversione implicita in una struttura di [**\_ matrici di \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) . Poiché D3D12 \_ RT \_ Format \_ Array è il tipo sottostante di CD3DX12 \_ Depth \_ stencil \_ DESC1, l'oggetto viene semplicemente restituito come \_ \_ riferimento alla matrice di formato const D3D12 RT \_ a se stesso.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Matrice di \_ formato D3D12 RT \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





