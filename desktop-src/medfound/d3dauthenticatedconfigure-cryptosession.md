---
description: Associa una sessione crittografica a un dispositivo decodificatore DirectX Video Acceleration 2 (DXVA-2) e a un dispositivo Direct3D.
ms.assetid: d40fead7-8a86-426e-933e-13df21cdf50b
title: D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION (D3d9types. h)
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
ms.openlocfilehash: 4b6fda19aef9629214aaa410fd43c4d64f16dd29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305432"
---
# <a name="d3dauthenticatedconfigure_cryptosession"></a>\_CRYPTOSESSION D3DAUTHENTICATEDCONFIGURE

Associa una sessione crittografica a un dispositivo decodificatore DirectX Video Acceleration 2 (DXVA-2) e a un dispositivo Direct3D.



| Requisito | Valore |
|--------------|-----------------------------------------------------------------------------------------------------------|
| GUID comando | **\_CRYPTOSESSION D3DAUTHENTICATEDCONFIGURE**                                                              |
| Dati di input   | [**\_CONFIGURECRYPTOSESSION D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-configurecryptosession.md) |



 

## <a name="remarks"></a>Commenti

Dopo l'invio di questo comando, è possibile inviare la query [D3DAUTHENTICATEDQUERY \_ OUTPUTID](d3dauthenticatedquery-outputid.md) per scoprire quali output video sono associati alla sessione di crittografia.

I tipi di canale seguenti supportano questo comando:

-   **\_D3d9 D3DAUTHENTICATEDCHANNEL**
-   **\_Software driver \_ D3DAUTHENTICATEDCHANNEL**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Comandi protezione del contenuto](content-protection-commands.md)
</dt> <dt>

[protezione del contenuto basate su GPU](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




