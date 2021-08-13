---
description: Imposta il livello di crittografia che viene eseguito prima che il contenuto protetto diventi accessibile alla CPU o al bus.
ms.assetid: 6de6c4a3-705a-4420-b9f4-8d4d442b23bf
title: D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE (D3d9types.h)
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
ms.openlocfilehash: f785931cf70ae48082cb45c436dd1c50b7c329fef61619738a3ef0a08240d7b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742648"
---
# <a name="d3dauthenticatedconfigure_encryptionwhenaccessible"></a>D3DAUTHENTICATEDCONFIGURARE \_ LA CRITTOGRAFIAWHENACCESSIBLE

Imposta il livello di crittografia che viene eseguito prima che il contenuto protetto diventi accessibile alla CPU o al bus.



| Requisito | Valore |
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| GUID del comando | **D3DAUTHENTICATEDCONFIGURARE \_ LA CRITTOGRAFIAWHENACCESSIBLE**                                                                     |
| Dati di input   | [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMPRESSEDENCRYPTION**](d3dauthenticatedchannel-configureuncompressedencryption.md) |



 

## <a name="remarks"></a>Commenti

I tipi di canale seguenti supportano questa query:

-   **HARDWARE DEL DRIVER D3DAUTHENTICATEDCHANNEL \_ \_**
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

 

 




