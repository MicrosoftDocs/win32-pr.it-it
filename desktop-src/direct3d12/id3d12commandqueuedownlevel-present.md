---
title: Metodo ID3D12CommandQueueDownlevel::P resent
description: Copia il contenuto da una risorsa Texture2D Direct3D 12 in una finestra. | Metodo ID3D12CommandQueueDownlevel::P resent
keywords:
- Metodo Present
- Metodo Present, interfaccia ID3D12CommandQueueDownlevel
- INTERFACCIA ID3D12CommandQueueDownlevel, metodo Present
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel.Present
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: b21a97d15d2666dcfe0a304f2393d6d14c5dbcc4142d8b42f43f295d8751614b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118529131"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a>Metodo ID3D12CommandQueueDownlevel::P resent

Copia il contenuto da una risorsa Texture2D Direct3D 12 in una finestra.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT Present
    ID3D12GraphicsCommandList *pOpenCommandList,
    ID3D12Resource *pSourceTex2D,
    HWND hWindow,
    D3D12_DOWNLEVEL_PRESENT_FLAGS Flags
);
```

## <a name="parameters"></a>Parametri

`pOpenCommandList`

Tipo: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Un elenco di comandi aperto, a cui Direct3D 12 accoda un comando Present, quindi chiude e invia per l'utente.

`pSourceTex2D`

Tipo: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***

Risorsa contenente il contenuto desiderato da visualizzare, con dimensione [**D3D12 \_ RESOURCE \_ DIMENSION \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)e un formato tra i seguenti.

* DXGI_FORMAT_R16G16B16A16_FLOAT
* DXGI_FORMAT_R10G10B10A2_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM_SRGB
* DXGI_FORMAT_B8G8R8X8_UNORM
* DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM_SRGB

`hWindow`

Tipo: **[HWND](/windows/desktop/WinProg/windows-data-types)**

Handle per la finestra in cui deve essere visualizzato il contenuto.

`Flags`

Tipo: FLAG PRESENTI DI LIVELLO INFERIORE **[ \_ \_ \_ D3D12](d3d12_downlevel_present_flags.md)**

Flag per modificare **l'operazione** Present.

## <a name="return-value"></a>Valore restituito

Restituisce **S_OK** in caso di esito positivo oppure restituisce un HRESULT con esito negativo.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------|------------------|
| Intestazione | d3d12downlevel.h |
| DLL    | D3D12.dll (solo Windows 7) |

## <a name="see-also"></a>Vedi anche
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Interfacce Direct3D 12 Windows 7](direct3d-12on7-interfaces.md)
* [Informazioni di riferimento su Direct3D 12 Windows 7 (d3d12downlevel.h)](direct3d-12on7-reference.md)
* [Direct3D 12 in Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
