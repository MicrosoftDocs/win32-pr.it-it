---
title: ID3D12CommandQueueDownlevel::P metodo reinviato
description: Copia il contenuto da una risorsa Direct3D 12 Texture2D in una finestra. | ID3D12CommandQueueDownlevel::P metodo reinviato
keywords:
- Metodo Present
- Metodo Present, interfaccia ID3D12CommandQueueDownlevel
- Interfaccia ID3D12CommandQueueDownlevel, metodo Present
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
ms.openlocfilehash: a6c74685911e52a671eaeb02645754a45b8d647e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323125"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a>ID3D12CommandQueueDownlevel::P metodo reinviato

Copia il contenuto da una risorsa Direct3D 12 Texture2D in una finestra.

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

Elenco di comandi aperti, che consente a Direct3D 12 di accodare un comando presente in e quindi di chiuderlo e inviarlo.

`pSourceTex2D`

Tipo: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***

Risorsa contenente il contenuto desiderato da visualizzare, con dimensione [**D3D12 della \_ dimensione della risorsa \_ \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)e un formato uno dei seguenti.

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

Tipo: **[D3D12 \_ i \_ \_ flag presenti](d3d12_downlevel_present_flags.md) di livello inferiore**

Flag per modificare l'operazione **corrente** .

## <a name="return-value"></a>Valore restituito

Restituisce **S_OK** in caso di esito positivo, altrimenti un HRESULT non riuscito.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------|------------------|
| Intestazione | d3d12downlevel. h |
| DLL    | D3D12.dll (solo Windows 7) |

## <a name="see-also"></a>Vedi anche
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Interfacce Direct3D 12 su Windows 7](direct3d-12on7-interfaces.md)
* [Guida di riferimento a Direct3D 12 per Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 in Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
