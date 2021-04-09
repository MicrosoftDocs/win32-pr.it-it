---
description: Consente la decodifica con accelerazione hardware da un dispositivo Direct3D 9 usando la versione 1,0 di DirectX Video Acceleration (DXVA).
ms.assetid: abe3beac-f3f8-413d-8b83-9da3340b19ac
title: Interfaccia IDirect3DVideoDevice9 (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 89afef6f39b3aa196d8b1013e3d8873e329ce6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130339"
---
# <a name="idirect3dvideodevice9-interface"></a>Interfaccia IDirect3DVideoDevice9

Consente la decodifica con accelerazione hardware da un dispositivo Direct3D 9 usando la versione 1,0 di DirectX Video Acceleration (DXVA).

## <a name="when-to-use"></a>Utilizzo

Questa interfaccia non è destinata all'utilizzo generale dell'applicazione. I filtri del decodificatore DirectShow devono usare l'interfaccia [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , non **IDirect3DVideoDevice9**. I pin di input del filtro VMR (video Mixing Renderer) e del filtro overlay mixer espongono **IAMVideoAccelerator**.

## <a name="members"></a>Membri

L'interfaccia **IDirect3DVideoDevice9** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirect3DVideoDevice9** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDirect3DVideoDevice9** dispone di questi metodi.



| Metodo                                                                                   | Descrizione                                                                                                                       |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md)                       | Crea un dispositivo di decodificatore DXVA.<br/>                                                                                         |
| [**CreateSurface**](idirect3dvideodevice9-createsurface.md)                             | Crea una superficie compressa per la decodifica DXVA.<br/>                                                                        |
| [**GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) | Ottiene informazioni sui buffer compressi necessari per la decodifica con accelerazione hardware.<br/>                                |
| [**GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md)                               | Ottiene un elenco dei profili DXVA supportati dal driver di visualizzazione.<br/>                                             |
| [**GetDXVAInternalInfo**](idirect3dvideodevice9-getdxvainternalinfo.md)                 | Esegue una query per la quantità di memoria Scratch che l'HAL (Hardware Abstraction Layer) alloca per l'uso privato. <br/> |
| [**GetUncompressedDXVAFormats**](idirect3dvideodevice9-getuncompresseddxvaformats.md)   | Ottiene un elenco di formati di pixel non compressi di cui è possibile eseguire il rendering utilizzando un profilo DXVA specificato.<br/>                         |



 

## <a name="remarks"></a>Commenti

Per ottenere un puntatore a questa interfaccia, chiamare **QueryInterface** su un puntatore [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) o [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) .

Questa interfaccia supporta solo DXVA 1,0. Non supporta DXVA 2,0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce video Direct3D](direct3d-video-interfaces.md)
</dt> <dt>

[Accelerazione video DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Specifica DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
