---
description: Associa una sessione di crittografia a un dispositivo decodificatore DXVA-2 (DirectX Video Acceleration 2) e a un dispositivo Direct3D.
ms.assetid: d40fead7-8a86-426e-933e-13df21cdf50b
title: D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 3e1df4b58750d5b2d82eb518d5dfc0ef24bdbe4e5569ebcaf708b8df60691d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449441"
---
# <a name="d3dauthenticatedconfigure_cryptosession"></a>D3DAUTHENTICATEDCONFIGURARE \_ CRYPTOSESSION

Associa una sessione di crittografia a un dispositivo decodificatore DXVA-2 (DirectX Video Acceleration 2) e a un dispositivo Direct3D.



| Requisito | Valore |
|--------------|-----------------------------------------------------------------------------------------------------------|
| GUID del comando | **D3DAUTHENTICATEDCONFIGURARE \_ CRYPTOSESSION**                                                              |
| Dati di input   | [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) |



 

## <a name="remarks"></a>Commenti

Dopo l'invio di questo comando, è possibile inviare la query [D3DAUTHENTICATEDQUERY \_ OUTPUTID](d3dauthenticatedquery-outputid.md) per individuare gli output video associati alla sessione di crittografia.

I tipi di canale seguenti supportano questo comando:

-   **D3DAUTHENTICATEDCHANNEL \_ D3D9**
-   **SOFTWARE DEL DRIVER D3DAUTHENTICATEDCHANNEL \_ \_**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[protezione del contenuto comandi](content-protection-commands.md)
</dt> <dt>

[Criteri basati su GPU protezione del contenuto](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




