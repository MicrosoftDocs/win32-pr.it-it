---
description: Creare il migliore dispositivo Direct3D e una catena di scambio.
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: Funzione D3DX10CreateDeviceAndSwapChain (D3DX10Core. h)
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
ms.openlocfilehash: fe71aeae91f8c43966e0fda2d2f430c7908f2855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355549"
---
# <a name="d3dx10createdeviceandswapchain-function"></a>D3DX10CreateDeviceAndSwapChain (funzione)

Creare il migliore dispositivo Direct3D e una catena di scambio.

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

*pAdapter* \[ in\]
</dt> <dd>

Tipo: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Puntatore a un [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).

</dd> <dt>

*DriverType* \[ in\]
</dt> <dd>

Tipo: **[ **\_ \_ tipo di driver D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

Tipo di driver per il dispositivo. Vedere [**\_ \_ tipo di driver D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).

</dd> <dt>

*Software* \[ di in\]
</dt> <dd>

Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**

Handle per la DLL che implementa un rasterizzatore software. Deve essere **null** se DriverType è non software. Il HMODULE di una DLL può essere ottenuto con [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)o [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

facoltativo. Flag di creazione del dispositivo (vedere [**D3D10 \_ Create \_ Device \_ flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) che Abilita i [livelli API](d3d10-graphics-programming-guide-api-features-layers.md). Questi flag possono essere OR bit per bit.

</dd> <dt>

*pSwapChainDesc* \[ in\]
</dt> <dd>

Tipo: **[ **DXGI \_ scambio \_ catena \_ desc**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***

Descrizione della catena di scambio. Vedere [**DXGI \_ swap \_ Chain \_ desc**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).

</dd> <dt>

*ppSwapChain* \[ out\]
</dt> <dd>

Tipo: **[ **IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***

Indirizzo di un puntatore a un [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).

</dd> <dt>

*ppDevice* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Indirizzo di un puntatore a un' [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) che riceverà il dispositivo appena creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Questo metodo restituisce uno dei seguenti [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Per creare il dispositivo migliore, questo metodo implementa più di un'opzione di creazione del dispositivo. In primo luogo, il metodo tenta di creare un dispositivo 10,1 (e una catena di scambio). Se l'operazione ha esito negativo, il metodo tenta di creare un dispositivo 10,0. Se l'operazione ha esito negativo, il metodo avrà esito negativo. Se l'applicazione deve creare solo un dispositivo 10,1 o solo un dispositivo 10,0, usare queste API:

-   Usare [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) per creare un dispositivo Direct3D 10,0 (solo) e una catena di scambio.
-   Usare [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) per creare un dispositivo Direct3D 10,1 (solo) e una catena di scambio.

Questo metodo richiede Windows Vista Service Pack 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
