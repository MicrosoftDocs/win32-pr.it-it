---
description: Creare il miglior dispositivo Direct3D e una catena di scambio.
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: Funzione D3DX10CreateDeviceAndSwapChain (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDeviceAndSwapChain
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: aa92b0fd7efb9c6f457fd035fad28992d965a4cf2f6fdad39936292f7a70a996
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852371"
---
# <a name="d3dx10createdeviceandswapchain-function"></a>Funzione D3DX10CreateDeviceAndSwapChain

Creare il miglior dispositivo Direct3D e una catena di scambio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateDeviceAndSwapChain(
  _In_  IDXGIAdapter         *pAdapter,
  _In_  D3D10_DRIVER_TYPE    DriverType,
  _In_  HMODULE              Software,
  _In_  UINT                 Flags,
  _In_  DXGI_SWAP_CHAIN_DESC *pSwapChainDesc,
  _Out_ IDXGISwapChain       **ppSwapChain,
  _Out_ ID3D10Device         **ppDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAdapter* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Puntatore a [**un oggetto IDXGIAdapter.**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)

</dd> <dt>

*DriverType* \[ Pollici\]
</dt> <dd>

Tipo: **[ **TIPO DI \_ DRIVER \_ D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

Tipo di driver per il dispositivo. Vedere [**TIPO DI \_ DRIVER \_ D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).

</dd> <dt>

*Software* \[ Pollici\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle per la DLL che implementa un rasterizzatore software. Deve essere **NULL se** DriverType non è software. Il modulo HMODULE di una DLL può essere ottenuto [con LoadLibrary,](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)o [GetModuleHandle.](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

facoltativo. Flag di creazione del dispositivo (vedere [**D3D10 \_ CREATE \_ DEVICE \_ FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) che abilitano i [livelli API](d3d10-graphics-programming-guide-api-features-layers.md). Questi flag possono essere OR bit per bit insieme.

</dd> <dt>

*pSwapChainDesc* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DXGI \_ SWAP \_ CHAIN \_ DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***

Descrizione della catena di scambio. Vedere [**DXGI \_ SWAP CHAIN \_ \_ DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).

</dd> <dt>

*ppSwapChain* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***

Indirizzo di un puntatore a [**un oggetto IDXGISwapChain.**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)

</dd> <dt>

*ppDevice* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Indirizzo di un puntatore a [**un'interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) che riceverà il dispositivo appena creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Questo metodo restituisce uno dei codici [restituiti Direct3D 10 seguenti.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Per creare il dispositivo migliore, questo metodo implementa più di un'opzione di creazione del dispositivo. In primo luogo, il metodo tenta di creare un dispositivo 10.1 (e la catena di scambio). In caso di errore, il metodo tenta di creare un dispositivo 10.0. Se l'operazione ha esito negativo, il metodo avrà esito negativo. Se l'applicazione deve creare solo un dispositivo 10.1 o solo un dispositivo 10.0, usare invece queste API:

-   Usare [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) per creare un dispositivo Direct3D 10.0 (solo) e una catena di scambio.
-   Usare [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) per creare un dispositivo Direct3D 10.1 (solo) e una catena di scambio.

Questo metodo richiede Windows Vista Service Pack 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[per utilizzo generico funzioni](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
