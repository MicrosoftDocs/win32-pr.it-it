---
description: Contiene i dati di input per un \_ comando D3DAUTHENTICATEDCONFIGURE SHAREDRESOURCE.
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: Struttura D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7cbbb1645b232195e1cdb12e859234339ddda287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305452"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a>\_Struttura D3DAUTHENTICATEDCHANNEL CONFIGURESHAREDRESOURCE

Contiene i dati di input per un comando [**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) .

Per inviare questa query, chiamare [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT       Parameters;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentiferType;
  HANDLE                                        ProcessHandle;
  BOOL                                          AllowAccess;
} D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE;
```



## <a name="members"></a>Members

<dl> <dt>

**Parametri**
</dt> <dd>

D3DAUTHENTICATEDCHANNEL configura la struttura di [**\_ \_ input**](d3dauthenticatedchannel-configure-input.md) che contiene il GUID del comando e altri dati.

</dd> <dt>

**ProcessIdentiferType**
</dt> <dd>

Valore [**D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) che specifica il tipo di processo. Per specificare il processo di Gestione finestre desktop (DWM), impostare questo membro su **PROCESSIDTYPE \_ DWM**. In caso contrario, impostare questo membro su **PROCESSIDTYPE \_ handle** e impostare il membro **ProcessHandle** su un handle valido.

</dd> <dt>

**ProcessHandle**
</dt> <dd>

Handle di processo. Se il membro **ProcessIdentifier** è uguale **all' \_ handle PROCESSTIDTYPE**, il membro **ProcessHandle** specifica un handle per un processo. In caso contrario, il valore viene ignorato.

</dd> <dt>

**AllowAccess**
</dt> <dd>

Se **true**, il processo specificato ha accesso alle risorse condivise limitate.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture video Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




