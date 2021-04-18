---
description: Creare il migliore dispositivo Direct3D 10 che rappresenta la scheda di visualizzazione. Se è possibile creare un dispositivo compatibile con Direct3D 10,1, sarà possibile acquisire un puntatore di interfaccia ID3D10Device1 dal puntatore all'interfaccia del dispositivo restituito.
ms.assetid: 1af8f4e5-a59e-403a-95d2-069b91bad93e
title: Funzione D3DX10CreateDevice (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDevice
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 38236a48cdd5197f7f19ef9be3f6fc0f1faca72c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323312"
---
# <a name="d3dx10createdevice-function"></a>D3DX10CreateDevice (funzione)

Creare il migliore dispositivo Direct3D 10 che rappresenta la scheda di visualizzazione. Se è possibile creare un dispositivo compatibile con Direct3D 10,1, sarà possibile acquisire un puntatore di [**interfaccia ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) dal puntatore all'interfaccia del dispositivo restituito.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateDevice(
  _In_  IDXGIAdapter      *pAdapter,
  _In_  D3D10_DRIVER_TYPE DriverType,
  _In_  HMODULE           Software,
  _In_  UINT              Flags,
  _Out_ ID3D10Device      **ppDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAdapter* \[ in\]
</dt> <dd>

Tipo: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Puntatore alla scheda di visualizzazione (vedere l'interfaccia [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) ) quando si crea un dispositivo hardware. in caso contrario, impostare questo parametro su **null**. Se durante la creazione di un dispositivo hardware viene specificato **null** , Direct3D utilizzerà il primo Adapter enumerato dall'interfaccia [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) .

</dd> <dt>

*DriverType* \[ in\]
</dt> <dd>

Tipo: **[ **\_ \_ tipo di driver D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

Il tipo di driver del dispositivo (vedere l'enumerazione del [**\_ \_ tipo di driver D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) ). Il tipo di driver determina il tipo di dispositivo che si creerà.

</dd> <dt>

*Software* \[ di in\]
</dt> <dd>

Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**

Handle per un modulo caricato che implementa un driver software, ad esempio D3D10Ref.dll. Per ottenere un handle, chiamare la funzione [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Flag di creazione del dispositivo (vedere l'enumerazione [**D3D10 \_ Create \_ Device \_ flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) ) che Abilita i [livelli API](d3d10-graphics-programming-guide-api-features-layers.md). Questi flag possono essere OR bit per bit.

</dd> <dt>

*ppDevice* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Indirizzo di un puntatore al dispositivo creato (vedere l'interfaccia [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Questa funzione restituisce uno dei seguenti [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Questa funzione tenta di creare il dispositivo migliore per l'hardware. In primo luogo, la funzione tenta di creare un dispositivo 10,1. Se non è possibile creare un dispositivo 10,1, la funzione tenta di creare un dispositivo 10,0. Se nessuno dei due dispositivi viene creato correttamente, la funzione restituisce E ha \_ esito negativo.

Se l'applicazione deve creare solo un dispositivo 10,1 o un dispositivo 10,0, usare invece le funzioni seguenti:

-   Usare la funzione [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) per creare solo un dispositivo Direct3D 10,0.
-   Usare la funzione [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) per creare solo un dispositivo Direct3D 10,1.
-   Usare la funzione [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) per ottenere un puntatore a interfaccia [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) da un puntatore a interfaccia [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .

Un dispositivo Direct3D 10,1 può essere creato solo in computer che eseguono Windows Vista Service Pack 1 o versione successiva e con hardware compatibile con Direct3D 10,1 installato. Tuttavia, è lecito chiamare questa funzione nei computer che eseguono qualsiasi versione di Windows in cui è installata la DLL D3DX10.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
