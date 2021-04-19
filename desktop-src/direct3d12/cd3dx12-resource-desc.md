---
title: Struttura CD3DX12_RESOURCE_DESC (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura di descrizione della risorsa D3D12 \_ .
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- Struttura CD3DX12_RESOURCE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b341646b2dee7f469235c0b0bc9bb4550e56ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323565"
---
# <a name="cd3dx12_resource_desc-structure"></a>\_Struttura desc della risorsa CD3DX12 \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ Descrizione della risorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_RESOURCE_DESC  : public D3D12_RESOURCE_DESC{
                        CD3DX12_RESOURCE_DESC();
                        explicit CD3DX12_RESOURCE_DESC(const D3D12_RESOURCE_DESC& o);
                        CD3DX12_RESOURCE_DESC(D3D12_RESOURCE_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12_TEXTURE_LAYOUT layout, D3D12_RESOURCE_FLAGS flags);
  CD3DX12_RESOURCE_DESC static inline Buffer(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE);
  CD3DX12_RESOURCE_DESC static inline Buffer(UINT64 width, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex1D(DXGI_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex2D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex3D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  UINT16                inline Depth() const;
  UINT16                inline ArraySize() const;
  UINT8                 inline PlaneCount(ID3D12Device* pDevice) const;
  UINT                  inline Subresources(ID3D12Device* pDevice) const;
  UINT                  inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice);
                        operator const D3D12_RESOURCE_DESC&() const;
                        operator == (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
                        operator !=  (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 della \_ risorsa \_ DESC ()**
</dt> <dd>

Crea un'istanza nuova, non inizializzata, di una \_ Descrizione della risorsa CD3DX12 \_ .

</dd> <dt>

**Descrizione della risorsa CD3DX12 esplicita \_ \_ (const D3D12 \_ Resource \_ desc& o)**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione della risorsa CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ Descrizione della risorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .

</dd> <dt>

**CD3DX12 \_ Resource \_ DESC (dimensione della \_ dimensione della risorsa D3D12 \_ , allineamento UInt64, lunghezza UInt64, altezza uint, UInt16 depthOrArraySize, UInt16 mipLevels, \_ formato di formato DXGI, uint sampleCount, uint SAMPLEQUALITY, \_ \_ layout layout trama D3D12, \_ flag flag di risorse D3D12 \_ )**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione della risorsa CD3DX12 \_ , inizializzando i parametri seguenti:

[**D3D12 \_ Dimensione della \_ dimensione della risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)

Allineamento UINT64

Larghezza UINT64

Altezza UINT

UINT16 depthOrArraySize

UINT16 mipLevels

[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

SampleCount UINT

SampleQuality UINT

[**D3D12 \_ Layout \_ layout trama**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)

[**D3D12 \_ Flag \_ flag di risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags)

</dd> <dt>

**Buffer inline statico (const D3D12 \_ Resource \_ allocation \_ info& resAllocInfo, D3D12 resource flags \_ \_ Flags = D3D12 \_ Resource \_ flag \_ None)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ \_ \_ Informazioni sull'allocazione delle risorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

consenso esplicito [**D3D12 \_ Flag \_ di risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = D3D12 \_ Resource \_ flag \_ None

</dd> <dt>

**Buffer inline statico (larghezza UINT64, flag di \_ risorsa D3D12 \_ flag = \_ D3D12 \_ flag \_ di risorsa None, allineamento UInt64 = 0)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

Larghezza UINT64

consenso esplicito [**D3D12 \_ Flag \_ di risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = D3D12 \_ Resource \_ flag \_ None

consenso esplicito Allineamento UINT64 = 0

</dd> <dt>

**static inline Tex1D (formato DXGI \_ , lunghezza UInt64, UInt16 arraySize = 1, UInt16 mipLevels = 0, D3D12 \_ Flags resource flags \_ = D3D12 \_ Resource \_ flag \_ None, D3D12 texture layout layout \_ \_ = D3D12 \_ texture \_ layout \_ Unknown, UInt64 Alignment = 0)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Larghezza UINT64

consenso esplicito UINT16 arraySize = 1

consenso esplicito UINT16 mipLevels = 0

consenso esplicito [**D3D12 \_ Flag \_ di risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = D3D12 \_ Resource \_ flag \_ None

consenso esplicito [**D3D12 \_ Layout \_ layout trama**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = \_ layout trama \_ D3D12 \_ sconosciuto

consenso esplicito Allineamento UINT64 = 0

</dd> <dt>

**static inline Tex2D (formato DXGI \_ , lunghezza UInt64, altezza uint, UInt16 arraySize = 1, UInt16 mipLevels = 0, uint sampleCount = 1, uint sampleQuality = 0, D3D12 \_ flag di risorse \_ flag = D3D12 \_ Resource \_ flag \_ None, D3D12 \_ texture layout layout \_ = D3D12 \_ texture \_ layout \_ Unknown, UInt64 Alignment = 0)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Larghezza UINT64

Altezza UINT

consenso esplicito UINT16 arraySize = 1

consenso esplicito UINT16 mipLevels = 0

consenso esplicito UINT sampleCount = 1

consenso esplicito UINT sampleQuality = 0

consenso esplicito [**D3D12 \_ Flag \_ di risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = D3D12 \_ Resource \_ flag \_ None

consenso esplicito [**D3D12 \_ Layout \_ layout trama**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = \_ layout trama \_ D3D12 \_ sconosciuto

consenso esplicito Allineamento UINT64 = 0

</dd> <dt>

**static inline Tex3D (formato DXGI \_ , lunghezza UInt64, altezza uint, profondità UInt16, UInt16 mipLevels = 0, D3D12 \_ flag di risorsa \_ flag = D3D12 \_ Resource \_ flag \_ None, D3D12 \_ texture layout layout \_ = D3D12 \_ texture \_ layout \_ Unknown, UInt64 allineamento = 0)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Larghezza UINT64

Altezza UINT

Profondità UINT16

consenso esplicito UINT16 mipLevels = 0

consenso esplicito [**D3D12 \_ Flag \_ di risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) Flags = D3D12 \_ Resource \_ flag \_ None

consenso esplicito [**D3D12 \_ Layout \_ layout trama**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = \_ layout trama \_ D3D12 \_ sconosciuto

consenso esplicito Allineamento UINT64 = 0

</dd> <dt>

**Profondità inline () const**
</dt> <dd>

Se Dimension = = [**D3D12 \_ della \_ dimensione della risorsa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D, restituisce DepthOrArraySize. Se Dimension! = D3D12 \_ della \_ dimensione della risorsa \_ TEXTURE3D, restituisce 1.

</dd> <dt>

**inline ArraySize () const**
</dt> <dd>

Se Dimension! = D3D12 \_ della \_ dimensione della risorsa \_ TEXTURE3D, restituisce DepthOrArraySize. Se Dimension = = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, restituisce 1. Vedere [**la \_ \_ dimensione della risorsa D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D.

</dd> <dt>

**inline PlaneCount (ID3D12Device \* PDEVICE) const**
</dt> <dd>

Restituisce D3D12GetFormatPlaneCount (pDevice, Format). Vedere [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) e [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).

</dd> <dt>

**sottorisorse inline (ID3D12Device \* PDEVICE) const**
</dt> <dd>

Restituisce il numero di sottorisorse, calcolato come MipLevels \* ArraySize () \* PlaneCount (PDEVICE).

</dd> <dt>

**inline CalcSubresource (UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**
</dt> <dd>

Consente di calcolare un indice di una sottorisorsa usando [**D3D12CalcSubresource**](d3d12calcsubresource.md).

</dd> <dt>

**operator const D3D12 \_ Resource \_ desc& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> <dt>

**operator = = (const D3D12 \_ Resource \_ desc& l, const D3D12 \_ Resource \_ desc& r)**
</dt> <dd>

Restituisce true se tutti i membri di ogni struttura sono identici.

</dd> <dt>

**operator! = (const D3D12 \_ Resource \_ desc& l, const D3D12 \_ Resource \_ desc& r)**
</dt> <dd>

Restituisce false se tutti i membri di ogni struttura sono identici.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Descrizione della risorsa D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

