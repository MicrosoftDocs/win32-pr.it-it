---
description: Contiene i dati di input per il comando D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE.
ms.assetid: d2d0adff-5d4d-4af3-b6b8-b8c60a506142
title: D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION struttura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 661f4cd043a2337aa499aaa165c16d2e1fdf41f8e87826412250ea0fe85c47a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062001"
---
# <a name="d3dauthenticatedchannel_configureuncompressedencryption-structure"></a>Struttura D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMPRESSEDENCRYPTION

Contiene i dati di input [**per il comando D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE.**](d3dauthenticatedconfigure-encryptionwhenaccessible.md)

Per inviare questa query, chiamare [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  GUID                                    EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION;
```



## <a name="members"></a>Members

<dl> <dt>

**Parametri**
</dt> <dd>

Struttura [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT**](d3dauthenticatedchannel-configure-input.md) che contiene il GUID del comando e altri dati.

</dd> <dt>

**EncryptionGuid**
</dt> <dd>

GUID che specifica il tipo di crittografia da applicare.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture video Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




