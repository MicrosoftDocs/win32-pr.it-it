---
description: Rappresenta un acceleratore hardware per DirectX Video Acceleration (DXVA) 1,0.
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
title: Interfaccia IDirect3DDXVADevice9 (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 192f47b8161893f9517bc976452eb8836da4bb53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310836"
---
# <a name="idirect3ddxvadevice9-interface"></a>Interfaccia IDirect3DDXVADevice9

Rappresenta un acceleratore hardware per DirectX Video Acceleration (DXVA) 1,0.

## <a name="members"></a>Membri

L'interfaccia **IDirect3DDXVADevice9** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirect3DDXVADevice9** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDirect3DDXVADevice9** dispone di questi metodi.



| Metodo                                                  | Descrizione                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------|
| [**BeginFrame**](idirect3ddxvadevice9-beginframe.md)   | Inizia l'elaborazione per creare un'immagine decodificata.<br/>         |
| [**EndFrame**](idirect3ddxvadevice9-endframe.md)       | Termina l'elaborazione per creare un'immagine decodificata.<br/>           |
| [**Execute**](idirect3ddxvadevice9-execute.md)         | Esegue un'operazione di decodifica DXVA. <br/>                       |
| [**QueryStatus**](idirect3ddxvadevice9-querystatus.md) | Esegue una query sullo stato di lettura/scrittura di una superficie di decodifica DXVA. <br/> |



 

## <a name="remarks"></a>Commenti

Per ottenere un puntatore a questa interfaccia, chiamare [**IDirect3DVideoDevice9:: CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce video Direct3D](direct3d-video-interfaces.md)
</dt> </dl>

 

 
