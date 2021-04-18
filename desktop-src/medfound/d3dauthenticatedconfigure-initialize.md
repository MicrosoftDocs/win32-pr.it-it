---
description: Inizializza il canale autenticato.
ms.assetid: a74edbaa-af57-4f8e-9974-f6053f59377f
title: D3DAUTHENTICATEDCONFIGURE_INITIALIZE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_INITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2cd3238b7a7eea27356ce76ec9c83bf8aea4d7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305428"
---
# <a name="d3dauthenticatedconfigure_initialize"></a>\_Inizializzazione D3DAUTHENTICATEDCONFIGURE

Inizializza il canale autenticato.



| Requisito | Valore |
|--------------|-----------------------------------------------------------------------------------------------------|
| GUID comando | **\_Inizializzazione D3DAUTHENTICATEDCONFIGURE**                                                           |
| Dati di input   | [**\_CONFIGUREINITIALIZE D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-configureinitialize.md) |



 

## <a name="remarks"></a>Commenti

Inviare questo comando una volta all'inizio della sessione. Questo comando può essere inviato solo una volta per ogni canale autenticato. Il numero di sequenza di input viene ignorato per questo comando.

I tipi di canale seguenti supportano questo comando:

-   **\_Hardware driver \_ D3DAUTHENTICATEDCHANNEL**
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

 

 




