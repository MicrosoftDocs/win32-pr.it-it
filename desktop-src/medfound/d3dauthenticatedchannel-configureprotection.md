---
description: Contiene i dati di input per un comando D3DAUTHENTICATEDCONFIGURE \_ PROTECTION.
ms.assetid: 44f37e78-7218-42be-a07a-5ab911f2ba21
title: D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION struttura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 3f7c202a29347d59bfaf79792806fcab56532637045985440c899eeae304a4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828771"
---
# <a name="d3dauthenticatedchannel_configureprotection-structure"></a>Struttura CONFIGUREPROTECTION D3DAUTHENTICATEDCHANNEL \_

Contiene i dati di input per [**un comando D3DAUTHENTICATEDCONFIGURE \_ PROTECTION.**](d3dauthenticatedconfigure-protection.md)

Per inviare questa query, chiamare [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT  Parameters;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS Protections;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION;
```



## <a name="members"></a>Members

<dl> <dt>

**Parametri**
</dt> <dd>

Struttura [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT**](d3dauthenticatedchannel-configure-input.md) che contiene il GUID del comando e altri dati.

</dd> <dt>

**Protezioni**
</dt> <dd>

Struttura [**D3DAUTHENTICATEDCHANNEL \_ PROTECTION \_ FLAGS**](d3dauthenticatedchannel-protection-flags.md) che specifica il livello di protezione.

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

 

 




