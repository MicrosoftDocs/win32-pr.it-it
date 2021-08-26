---
title: CD3DX12_RESOURCE_DESC struttura (D3dx12.h)
description: Struttura helper per consentire un'inizializzazione semplice di una struttura D3D12 \_ RESOURCE \_ DESC.
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- CD3DX12_RESOURCE_DESC struttura
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
ms.openlocfilehash: 5c9d92953abdb0cf77a7a55f7b64341b857a111baaef0d84d4d44855b02efb2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028301"
---
# <a name="cd3dx12_resource_desc-structure"></a>Struttura CD3DX12 \_ RESOURCE \_ DESC

Struttura helper per consentire un'inizializzazione semplice di [**una struttura D3D12 \_ RESOURCE \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)

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

**CD3DX12 \_ RESOURCE \_ DESC()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una risorsa DESC CD3DX12. \_ \_

</dd> <dt>

**explicit CD3DX12 \_ RESOURCE \_ DESC(const D3D12 \_ RESOURCE \_ DESC& o)**
</dt> <dd>

Crea una nuova istanza di una risorsa DESC CD3DX12, inizializzata con il contenuto di \_ \_ un'altra struttura [**D3D12 \_ RESOURCE \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)

</dd> <dt>

**CD3DX12 \_ RESOURCE \_ DESC(D3D12 \_ RESOURCE DIMENSION \_ dimension, UINT64 alignment, UINT64 width, UINT height, UINT depthOrArraySize, UINT16 mipLevels, DXGI \_ FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12 \_ TEXTURE LAYOUT layout \_ layout, D3D12 \_ RESOURCE FLAGS \_ flags)**
</dt> <dd>

Crea una nuova istanza di una risorsa DESC CD3DX12, \_ \_ inizializzando i parametri seguenti:

[**D3D12 \_ Dimensione RESOURCE \_ DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)

Allineamento UINT64

Larghezza UINT64

Altezza UINT

UINT16 depthOrArraySize

UINT16 mipLevels

[**DXGI \_ Formato FORMATO**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

UINT sampleCount

UINT sampleQuality

[**D3D12 \_ Layout \_ TEXTURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)

[**D3D12 \_ Flag \_ RESOURCE FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags)

</dd> <dt>

**static inline Buffer(const D3D12 \_ RESOURCE ALLOCATION INFO& \_ \_ resAllocInfo, D3D12 \_ RESOURCE FLAGS flags = \_ D3D12 \_ RESOURCE FLAG \_ \_ NONE)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

[**D3D12 \_ INFORMAZIONI \_ \_ SULL'ALLOCAZIONE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

(scelta esplicita) [**D3D12 \_ FLAG \_ DI RISORSE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = D3D12 RESOURCE FLAG \_ \_ \_ NONE

</dd> <dt>

**static inline Buffer(UINT64 width, D3D12 \_ RESOURCE FLAGS flags = \_ D3D12 \_ RESOURCE FLAG \_ \_ NONE, UINT64 alignment = 0)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

Larghezza UINT64

(scelta esplicita) [**D3D12 \_ FLAG \_ DI RISORSE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = D3D12 RESOURCE FLAG \_ \_ \_ NONE

(scelta esplicita) Allineamento UINT64 = 0

</dd> <dt>

**static inline Tex1D(DXGI \_ FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, \_ D3D12 RESOURCE FLAGS flags = \_ D3D12 \_ RESOURCE FLAG \_ \_ NONE, D3D12 \_ TEXTURE LAYOUT layout = \_ D3D12 \_ TEXTURE LAYOUT \_ \_ UNKNOWN, UINT64 alignment = 0)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

[**DXGI \_ Formato FORMATO**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Larghezza UINT64

(scelta esplicita) UINT16 arraySize = 1

(scelta esplicita) UINT16 mipLevels = 0

(scelta esplicita) [**D3D12 \_ FLAG \_ DI RISORSE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = D3D12 RESOURCE FLAG \_ \_ \_ NONE

(scelta esplicita) [**D3D12 \_ LAYOUT \_ TRAMA**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = LAYOUT TRAMA D3D12 \_ \_ \_ SCONOSCIUTO

(scelta esplicita) Allineamento UINT64 = 0

</dd> <dt>

**static inline Tex2D(DXGI \_ FORMAT format, Larghezza UINT64, altezza UINT, arraySize UINT16 = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, FLAG DI RISORSE D3D12 = FLAG DI RISORSA \_ \_ D3D12 \_ NONE, LAYOUT DI TRAMA \_ \_ D3D12 \_ = \_ D3D12 LAYOUT TEXTURE UNKNOWN, allineamento \_ \_ \_ UINT64 = 0)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

[**DXGI \_ Formato FORMATO**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Larghezza UINT64

Altezza UINT

(scelta esplicita) UINT16 arraySize = 1

(scelta esplicita) UINT16 mipLevels = 0

(scelta esplicita) UINT sampleCount = 1

(scelta esplicita) UINT sampleQuality = 0

(scelta esplicita) [**D3D12 \_ FLAG \_ DI RISORSE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = D3D12 RESOURCE FLAG \_ \_ \_ NONE

(scelta esplicita) [**D3D12 \_ LAYOUT \_ TRAMA**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = LAYOUT TRAMA D3D12 \_ \_ \_ SCONOSCIUTO

(scelta esplicita) Allineamento UINT64 = 0

</dd> <dt>

**static inline Tex3D(DXGI \_ FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, \_ D3D12 RESOURCE FLAGS flags = \_ D3D12 \_ RESOURCE FLAG \_ \_ NONE, D3D12 \_ TEXTURE LAYOUT layout = \_ D3D12 \_ TEXTURE LAYOUT \_ \_ UNKNOWN, UINT64 alignment = 0)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

[**DXGI \_ Formato FORMATO**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Larghezza UINT64

Altezza UINT

Profondità UINT16

(scelta esplicita) UINT16 mipLevels = 0

(scelta esplicita) [**D3D12 \_ FLAG \_ DI RISORSE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = D3D12 RESOURCE FLAG \_ \_ \_ NONE

(scelta esplicita) [**D3D12 \_ LAYOUT \_ TRAMA**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = LAYOUT TRAMA D3D12 \_ \_ \_ SCONOSCIUTO

(scelta esplicita) Allineamento UINT64 = 0

</dd> <dt>

**inline Depth() const**
</dt> <dd>

Se Dimension == [**D3D12 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D, restituisce DepthOrArraySize. Se Dimension != D3D12 \_ RESOURCE \_ DIMENSION \_ TEXTURE3D, restituisce 1.

</dd> <dt>

**inline ArraySize() const**
</dt> <dd>

Se Dimension != D3D12 \_ RESOURCE \_ DIMENSION \_ TEXTURE3D, restituisce DepthOrArraySize. Se Dimension == D3D12 \_ RESOURCE \_ DIMENSION \_ TEXTURE3D, restituisce 1. Vedere [**D3D12 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D.

</dd> <dt>

**inline PlaneCount(ID3D12Device \* pDevice) const**
</dt> <dd>

Restituisce D3D12GetFormatPlaneCount(pDevice, Format). Vedere [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) e [**ID3D12Device.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)

</dd> <dt>

**inline Subresources(ID3D12Device \* pDevice) const**
</dt> <dd>

Restituisce il numero di sottorisorse, calcolato come \* PlaneCount(pDevice) Di MipLevels \* ArraySize().

</dd> <dt>

**inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**
</dt> <dd>

Calcola un indice di sottorisorsa usando [**D3D12CalcSubresource.**](d3d12calcsubresource.md)

</dd> <dt>

**Operatore const D3D12 \_ RESOURCE \_ DESC&() const**
</dt> <dd>

Definisce l& operatore pass-by-reference per il tipo di struttura padre.

</dd> <dt>

**operatore == (const D3D12 \_ RESOURCE \_ DESC& l, const D3D12 \_ RESOURCE \_ DESC& r)**
</dt> <dd>

Restituisce true se tutti i membri di ogni struttura sono identici.

</dd> <dt>

**operatore != (const D3D12 \_ RESOURCE \_ DESC& l, const D3D12 \_ RESOURCE \_ DESC& r)**
</dt> <dd>

Restituisce false se tutti i membri di ogni struttura sono identici.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ RESOURCE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

