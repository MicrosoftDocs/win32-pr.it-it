---
description: Consente a un processo di aprire una risorsa condivisa o di disabilitare l'apertura di risorse condivise da un processo.
ms.assetid: 5fa2b88f-e946-436c-953e-04e0e338146c
title: D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7404a4bed3ac3b1d4002bb03c45d7732500b77e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225816"
---
# <a name="d3dauthenticatedconfigure_sharedresource"></a>\_SHAREDRESOURCE D3DAUTHENTICATEDCONFIGURE

Consente a un processo di aprire una risorsa condivisa o di disabilitare l'apertura di risorse condivise da un processo.



| Requisito | Valore |
|--------------|-------------------------------------------------------------------------------------------------------------|
| GUID comando | **\_SHAREDRESOURCE D3DAUTHENTICATEDCONFIGURE**                                                               |
| Dati di input   | [**\_CONFIGURESHAREDRESOURCE D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-configuresharedresource.md) |



 

## <a name="remarks"></a>Commenti

I tipi di canale seguenti supportano questa query:

-   **\_D3d9 driver \_ D3DAUTHENTICATEDCHANNEL**
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

 

 




