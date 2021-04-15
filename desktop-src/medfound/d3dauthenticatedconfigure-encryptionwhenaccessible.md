---
description: Imposta il livello di crittografia che viene eseguito prima che il contenuto protetto diventi accessibile alla CPU o al bus.
ms.assetid: 6de6c4a3-705a-4420-b9f4-8d4d442b23bf
title: D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8b624c26c81549372e0e09b4a08ce73f6cd3dd27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524593"
---
# <a name="d3dauthenticatedconfigure_encryptionwhenaccessible"></a>\_ENCRYPTIONWHENACCESSIBLE D3DAUTHENTICATEDCONFIGURE

Imposta il livello di crittografia che viene eseguito prima che il contenuto protetto diventi accessibile alla CPU o al bus.



| Requisito | Valore |
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| GUID comando | **\_ENCRYPTIONWHENACCESSIBLE D3DAUTHENTICATEDCONFIGURE**                                                                     |
| Dati di input   | [**\_CONFIGUREUNCOMPRESSEDENCRYPTION D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-configureuncompressedencryption.md) |



 

## <a name="remarks"></a>Commenti

I tipi di canale seguenti supportano questa query:

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

 

 




