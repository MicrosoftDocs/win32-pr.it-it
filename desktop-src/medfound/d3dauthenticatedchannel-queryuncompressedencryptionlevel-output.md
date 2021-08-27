---
description: Contiene la risposta a una query D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE.
ms.assetid: 66735ce3-c16b-4eca-9283-5d3bc37d73d3
title: D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT struttura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: aa9642a37237425f1d9236632fdf0c16bf226b3f2952928cceccf1b1c577d2e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061971"
---
# <a name="d3dauthenticatedchannel_queryuncompressedencryptionlevel_output-structure"></a>Struttura DI OUTPUT D3DAUTHENTICATEDCHANNEL \_ QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_

Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE.**](d3dauthenticatedquery-currentencryptionwhenaccessible.md)

Per inviare questa query, chiamare [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  GUID                                 EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Output**
</dt> <dd>

Struttura [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ OUTPUT**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (MAC) e altri dati.

</dd> <dt>

**EncryptionGuid**
</dt> <dd>

GUID che specifica il tipo di crittografia corrente.

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

 

 




