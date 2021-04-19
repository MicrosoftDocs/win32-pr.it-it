---
title: Struttura CD3DX12_SUBRESOURCE_FOOTPRINT (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura footprint della SOTTORISORSA D3D12 \_ .
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- Struttura CD3DX12_SUBRESOURCE_FOOTPRINT
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_FOOTPRINT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab58e9a007d736222d9525d7a064456a1a9a7f14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322202"
---
# <a name="cd3dx12_subresource_footprint-structure"></a>\_Struttura del footprint della SOTTORISORSA CD3DX12 \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ footprint della sottorisorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_SUBRESOURCE_FOOTPRINT  : public D3D12_SUBRESOURCE_FOOTPRINT{
   CD3DX12_SUBRESOURCE_FOOTPRINT();
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_SUBRESOURCE_FOOTPRINT &o);
   CD3DX12_SUBRESOURCE_FOOTPRINT(DXGI_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch);
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_RESOURCE_DESC& resDesc, UINT rowPitch);
   operator const D3D12_SUBRESOURCE_FOOTPRINT&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_Footprint delle sottorisorse CD3DX12 \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ footprint della SOTTORISORSA CD3DX12 \_ .

</dd> <dt>

**footprint della \_ SOTTORISORSA CD3DX12 esplicita \_ (CONSt D3D12 \_ subresource \_ footprint &o)**
</dt> <dd>

Crea una nuova istanza di un \_ footprint della SOTTORISORSA CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura [**\_ \_ footprint della sottorisorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .

</dd> <dt>

**\_Footprint della SOTTORISORSA CD3DX12 \_ ( \_ formato DXGI, lunghezza UINT, altezza UINT, profondità uint, uint rowPitch)**
</dt> <dd>

Crea una nuova istanza di un \_ footprint della SOTTORISORSA CD3DX12 \_ , inizializzando i parametri seguenti:

[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Lunghezza UINT

Altezza UINT

Profondità UINT

RowPitch UINT

</dd> <dt>

**\_footprint delle sottorisorse CD3DX12 esplicito \_ (const D3D12 \_ Resource \_ desc& resDesc, uint rowPitch)**
</dt> <dd>

Crea una nuova istanza di un \_ footprint della SOTTORISORSA CD3DX12 \_ , inizializzando i parametri seguenti:

[**D3D12 \_ \_Descrizione della risorsa**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc

RowPitch UINT

</dd> <dt>

**operatore const D3D12 \_ subresource \_ footprint& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Footprint delle sottorisorse D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

