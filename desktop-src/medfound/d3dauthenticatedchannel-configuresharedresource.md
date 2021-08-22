---
description: Contiene i dati di input per un comando D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE.
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE struttura (D3d9types.h)
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
ms.openlocfilehash: 0dbff67921f2ec6ad634c20b11b86b0384923db5548bcef113128fe5ede6bdd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742907"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a>Struttura D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE

Contiene i dati di input per [**un comando D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE.**](d3dauthenticatedconfigure-sharedresource.md)

Per inviare questa query, chiamare [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

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

Struttura [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT**](d3dauthenticatedchannel-configure-input.md) che contiene il GUID del comando e altri dati.

</dd> <dt>

**ProcessIdentiferType**
</dt> <dd>

Valore [**D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) che specifica il tipo di processo. Per specificare il processo Gestione finestre desktop (DWM), impostare questo membro su **PROCESSIDTYPE \_ DWM**. In caso contrario, impostare questo membro su **PROCESSIDTYPE \_ HANDLE** e impostare il **membro ProcessHandle** su un handle valido.

</dd> <dt>

**ProcessHandle**
</dt> <dd>

Handle di processo. Se il **membro ProcessIdentifier** è uguale a **PROCESSTIDTYPE \_ HANDLE,** il membro **ProcessHandle** specifica un handle per un processo. In caso contrario, il valore viene ignorato.

</dd> <dt>

**AllowAccess**
</dt> <dd>

Se **TRUE,** il processo specificato ha accesso alle risorse condivise limitate.

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

 

 




