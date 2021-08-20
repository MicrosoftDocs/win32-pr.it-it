---
description: Contiene la risposta a una query D3DAUTHENTICATEDQUERY \_ CHANNELTYPE.
ms.assetid: 547f7f26-2b9d-48b1-97cc-84a2202c3900
title: D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT struttura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 86b099d2c0219f936c926cf6fb22bf8ed7184f7d6a6565279fb1bf32eb01f321
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880376"
---
# <a name="d3dauthenticatedchannel_querychanneltype_output-structure"></a>Struttura \_ DI OUTPUT QUERYCHANNELTYPE D3DAUTHENTICATEDCHANNEL \_

Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE.**](d3dauthenticatedquery-channeltype.md)

Per inviare questa query, [**chiamare IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DAUTHENTICATEDCHANNELTYPE          ChannelType;
} D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Output**
</dt> <dd>

Struttura [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ OUTPUT**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (MAC) e altri dati.

</dd> <dt>

**Tipo di canale**
</dt> <dd>

Valore [**D3DAUTHENTICATEDCHANNELTYPE**](d3dauthenticatedchanneltype.md) che specifica il tipo di canale.

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

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




