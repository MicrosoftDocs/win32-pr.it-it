---
description: Specifica il tipo di canale autenticato Direct3D.
ms.assetid: 99a7664e-b0c8-4e66-ad3b-c6ad039ef6eb
title: Enumerazione D3DAUTHENTICATEDCHANNELTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5c0cab8a0a208bfb1a005166740dcc64c319c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305433"
---
# <a name="d3dauthenticatedchanneltype-enumeration"></a>Enumerazione D3DAUTHENTICATEDCHANNELTYPE

Specifica il tipo di canale autenticato Direct3D.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  D3DAUTHENTICATEDCHANNEL_D3D9             = 1,
  D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE  = 2,
  D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE  = 3
} D3DAUTHENTICATEDCHANNELTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**\_D3d9 D3DAUTHENTICATEDCHANNEL**
</dt> <dd>

Canale Direct3D 9. Questo canale fornisce la comunicazione con il runtime di Direct3D.

</dd> <dt>

<span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**\_Software driver \_ D3DAUTHENTICATEDCHANNEL**
</dt> <dd>

Canale driver software. Questo canale fornisce la comunicazione con un driver che implementa i meccanismi di protezione del contenuto nel software.

</dd> <dt>

<span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**\_Hardware driver \_ D3DAUTHENTICATEDCHANNEL**
</dt> <dd>

Canale driver hardware. Questo canale fornisce la comunicazione con un driver che implementa i meccanismi di protezione del contenuto nell'hardware della GPU.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>D3d9types. h (include d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni video Direct3D](direct3d-video-enumerations.md)
</dt> <dt>

[**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)
</dt> </dl>

 

 




