---
description: Ottenere un puntatore a interfaccia di dispositivo Direct3D 10.1 da un puntatore a interfaccia Direct3D 10.0.
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: Funzione D3DX10GetFeatureLevel1 (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetFeatureLevel1
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: c6511e0d3963e21f8950529b32cf8c3b414cc00b0625b97b2a9d569d1523c326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753171"
---
# <a name="d3dx10getfeaturelevel1-function"></a>Funzione D3DX10GetFeatureLevel1

Ottenere un puntatore a interfaccia di dispositivo Direct3D 10.1 da un puntatore a interfaccia Direct3D 10.0.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntatore al dispositivo Direct3D 10.0 (vedere [**l'interfaccia ID3D10Device).**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)

</dd> <dt>

*ppDevice* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***

Puntatore al dispositivo Direct3D 10.1 (vedere [**l'interfaccia ID3D10Device1).**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Questa funzione restituisce uno dei seguenti [codici restituiti di Direct3D 10.](d3d10-graphics-reference-returnvalues.md) Se è possibile acquisire un'interfaccia di dispositivo Direct3D 10.1, questa funzione ha esito positivo e passa un puntatore all'interfaccia 10.1 usando il *parametro ppDevice.* Se non è possibile acquisire un'interfaccia di dispositivo Direct3D 10.1, questa funzione restituisce E FAIL e non restituisce alcun valore \_ per il *parametro ppDevice.*

## <a name="remarks"></a>Commenti

Perché questa funzione abbia esito positivo, è necessario aver acquisito il puntatore [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) fornito usando una chiamata alla funzione [**D3DX10CreateDevice,**](d3dx10createdevice.md) alla funzione [**D3DX10CreateDeviceAndSwapChain,**](d3dx10createdeviceandswapchain.md) alla funzione [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) o alla funzione [**D3D10CreateDeviceAndSwapChain1.**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1)

È possibile creare un dispositivo Direct3D 10.1 solo in computer che eseguono Windows Vista Service Pack 1 o versione successiva e con hardware compatibile con Direct3D 10.1 installato. Questa funzione restituirà E \_ FAIL in tutti i computer che non soddisfare questi requisiti. È tuttavia possibile chiamare questa funzione in qualsiasi versione di Windows in cui è installata la DLL D3DX10.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Per utilizzo generico funzioni](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




