---
title: CD3DX12_RESOURCE_DESC1 struttura (D3dx12.h)
description: Struttura helper per consentire un'inizializzazione semplice di una [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) struttura .
keywords:
- CD3DX12_RESOURCE_DESC1 struttura
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2021
ms.openlocfilehash: 87fe62c475e1d961258671355c4c9be133bf0a41
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813240"
---
# <a name="cd3dx12_resource_desc1-structure"></a>CD3DX12_RESOURCE_DESC1 struttura

Struttura helper per consentire un'inizializzazione semplice di una [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) struttura .

## <a name="syntax"></a>Sintassi

```cpp
struct CD3DX12_RESOURCE_DESC1 : public D3D12_RESOURCE_DESC1
{
    CD3DX12_RESOURCE_DESC1();
    explicit CD3DX12_RESOURCE_DESC1(const D3D12_RESOURCE_DESC1& o) noexcept;
    CD3DX12_RESOURCE_DESC1(
        D3D12_RESOURCE_DIMENSION dimension,
        UINT64 alignment,
        UINT64 width,
        UINT height,
        UINT16 depthOrArraySize,
        UINT16 mipLevels,
        DXGI_FORMAT format,
        UINT sampleCount,
        UINT sampleQuality,
        D3D12_TEXTURE_LAYOUT layout,
        D3D12_RESOURCE_FLAGS flags,
        UINT samplerFeedbackMipRegionWidth = 0,
        UINT samplerFeedbackMipRegionHeight = 0,
        UINT samplerFeedbackMipRegionDepth = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Buffer(
        const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Buffer(
        UINT64 width,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        UINT64 alignment = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex1D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT16 arraySize = 1,
        UINT16 mipLevels = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex2D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT height,
        UINT16 arraySize = 1,
        UINT16 mipLevels = 0,
        UINT sampleCount = 1,
        UINT sampleQuality = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0,
        UINT samplerFeedbackMipRegionWidth = 0,
        UINT samplerFeedbackMipRegionHeight = 0,
        UINT samplerFeedbackMipRegionDepth = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex3D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT height,
        UINT16 depth,
        UINT16 mipLevels = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0) noexcept;
    inline UINT16 Depth() const noexcept;
    inline UINT16 ArraySize() const noexcept;
    inline UINT8 PlaneCount(_In_ ID3D12Device* pDevice) const noexcept;
    inline UINT Subresources(_In_ ID3D12Device* pDevice) const noexcept;
    inline UINT CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice) noexcept;
};
inline bool operator==(const D3D12_RESOURCE_DESC1& l, const D3D12_RESOURCE_DESC1& r) noexcept;
inline bool operator!=(const D3D12_RESOURCE_DESC1& l, const D3D12_RESOURCE_DESC1& r) noexcept;
```

## <a name="members"></a>Members

`CD3DX12_RESOURCE_DESC1`

Costruttore predefinito. Crea una nuova istanza non inizializzata di un **CD3DX12_RESOURCE_DESC1**.

`CD3DX12_RESOURCE_DESC1(const D3D12_RESOURCE_DESC1&)`

Costruttore che crea una nuova istanza di un **CD3DX12_RESOURCE_DESC1** inizializzato con il contenuto di una [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) struttura .

`CD3DX12_RESOURCE_DESC1(D3D12_RESOURCE_DIMENSION, UINT64, UINT64, UINT, UINT16, UINT16, DXGI_FORMAT, UINT, UINT, D3D12_TEXTURE_LAYOUT, D3D12_RESOURCE_FLAGS, UINT = 0, UINT = 0, UINT = 0)`

Costruttore che crea una nuova istanza di un **CD3DX12_RESOURCE_DESC1** inizializzato con i parametri passati.

`Buffer(const D3D12_RESOURCE_ALLOCATION_INFO&, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE)`

Funzione statica che costruisce e restituisce una nuova istanza di un **CD3DX12_RESOURCE_DESC1** inizializzata con questi valori.

|Membro dei dati|Valore|
|-|-|
|Dimensione|D3D12_RESOURCE_DIMENSION_BUFFER|
|Allineamento|*resAllocInfo*. Allineamento|
|Larghezza|*resAllocInfo*. SizeInBytes|
|Altezza|1|
|DepthOrArraySize|1|
|MipLevels|1|
|Formato|DXGI_FORMAT_UNKNOWN|
|SampleDesc.Count|1|
|SampleDesc.Quality|0|
|Layout|D3D12_TEXTURE_LAYOUT_ROW_MAJOR|
|Flags|*flags*|
|SamplerFeedbackMipRegion.Width|0|
|SamplerFeedbackMipRegion.Height|0|
|SamplerFeedbackMipRegion.Depth|0|

`Buffer(UINT64, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, UINT64 = 0)`

Funzione statica che costruisce e restituisce una nuova istanza di un **CD3DX12_RESOURCE_DESC1** inizializzata con questi valori.

|Membro dei dati|Valore|
|-|-|
|Dimensione|D3D12_RESOURCE_DIMENSION_BUFFER|
|Allineamento|*Allineamento*|
|Larghezza|*width*|
|Altezza|1|
|DepthOrArraySize|1|
|MipLevels|1|
|Formato|DXGI_FORMAT_UNKNOWN|
|SampleDesc.Count|1|
|SampleDesc.Quality|0|
|Layout|D3D12_TEXTURE_LAYOUT_ROW_MAJOR|
|Flags|*flags*|
|SamplerFeedbackMipRegion.Width|0|
|SamplerFeedbackMipRegion.Height|0|
|SamplerFeedbackMipRegion.Depth|0|

`Tex1D(DXGI_FORMAT, UINT64, UINT16 = 1, UINT16 = 0, D3D12_RESOURCE_FLAGS D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0)`

Funzione statica che costruisce e restituisce una nuova istanza di un **CD3DX12_RESOURCE_DESC1** inizializzata con questi valori.

|Membro dei dati|Valore|
|-|-|
|Dimensione|D3D12_RESOURCE_DIMENSION_TEXTURE1D|
|Allineamento|*Allineamento*|
|Larghezza|*width*|
|Altezza|1|
|DepthOrArraySize|*arraySize*|
|MipLevels|*mipLevels*|
|Formato|*format*|
|SampleDesc.Count|1|
|SampleDesc.Quality|0|
|Layout|*Layout*|
|Flags|*flags*|
|SamplerFeedbackMipRegion.Width|0|
|SamplerFeedbackMipRegion.Height|0|
|SamplerFeedbackMipRegion.Depth|0|

`Tex2D(DXGI_FORMAT, UINT64, UINT, UINT16 = 1, UINT16 = 0, UINT = 1, UINT = 0, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0, UINT = 0, UINT = 0, UINT = 0)`

Funzione statica che costruisce e restituisce una nuova istanza di **un** CD3DX12_RESOURCE_DESC1 inizializzata con questi valori.

|Membro dei dati|Valore|
|-|-|
|Dimensione|D3D12_RESOURCE_DIMENSION_TEXTURE2D|
|Allineamento|*Allineamento*|
|Larghezza|*width*|
|Altezza|*height*|
|DepthOrArraySize|*arraySize*|
|MipLevels|*mipLevels*|
|Formato|*format*|
|SampleDesc.Count|*sampleCount*|
|SampleDesc.Quality|*sampleQuality*|
|Layout|*Layout*|
|Flags|*flags*|
|SamplerFeedbackMipRegion.Width|*samplerFeedbackMipRegionWidth*|
|SamplerFeedbackMipRegion.Height|*samplerFeedbackMipRegionHeight*|
|SamplerFeedbackMipRegion.Depth|*samplerFeedbackMipRegionDepth*|

`Tex3D(DXGI_FORMAT, UINT64, UINT, UINT16, UINT16 = 0, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0)`

Funzione statica che costruisce e restituisce una nuova istanza di **un** CD3DX12_RESOURCE_DESC1 inizializzata con questi valori.

|Membro dei dati|Valore|
|-|-|
|Dimensione|D3D12_RESOURCE_DIMENSION_TEXTURE3D|
|Allineamento|*Allineamento*|
|Larghezza|*width*|
|Altezza|*height*|
|DepthOrArraySize|*Profondità*|
|MipLevels|*mipLevels*|
|Formato|*format*|
|SampleDesc.Count|1|
|SampleDesc.Quality|0|
|Layout|*Layout*|
|Flags|*flags*|
|SamplerFeedbackMipRegion.Width|0|
|SamplerFeedbackMipRegion.Height|0|
|SamplerFeedbackMipRegion.Depth|0|

`Depth`

Restituisce un **oggetto UINT16** contenente la profondità della risorsa.

`ArraySize`

Restituisce un **oggetto UINT16** contenente le dimensioni della matrice della risorsa.

`PlaneCount(ID3D12Device*)`

Restituisce un **oggetto UINT8** contenente il numero di piani per il formato della risorsa.

`Subresources(ID3D12Device*)`

Restituisce un **UINT** contenente il numero di sottorisorse nella risorsa.

`CalcSubresource(UINT, UINT, UINT)`

Caculates e restituisce un **UINT** contenente un indice di sottorisorsa per la risorsa in base ai parametri passati.

`operator==(const D3D12_RESOURCE_DESC1&, const D3D12_RESOURCE_DESC1&)`

Funzione gratuita che restituisce se i due parametri sono uguali a livello di `true` membro; in caso `false` contrario, .

`operator!=(const D3D12_RESOURCE_DESC1&, const D3D12_RESOURCE_DESC1&)`

Funzione gratuita che restituisce se i due parametri non sono uguali a livello `true` di membro; in caso `false` contrario, .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vedi anche

* [D3DX12_RESOURCE_DESC1](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1)
* [Strutture helper per Direct3D 12](helper-structures-for-d3d12.md)
