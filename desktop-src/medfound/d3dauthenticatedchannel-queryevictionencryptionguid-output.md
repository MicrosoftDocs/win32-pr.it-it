---
description: Contiene la risposta a una query D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID.
ms.assetid: afe73f8e-3304-470c-a37a-17b6c767b2c0
title: D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT struttura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 01624b35b7c1b29267b490204a2d814adec1c7075eaf23e746e6ade04ceb0c6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942771"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_output-structure"></a>Struttura DI OUTPUT D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_

Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID.**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)

Per inviare questa query, chiamare [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  UINT   EncryptionGuidIndex;
  GUID   EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**OUTPUT DELLE QUERY D3DAUTHENTICATEDCHANNEL \_ \_**
</dt> <dd>

Struttura [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ OUTPUT**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (MAC) e altri dati.

</dd> <dt>

**EncryptionGuidIndex**
</dt> <dd>

Indice del GUID di crittografia.

</dd> <dt>

**EncryptionGuid**
</dt> <dd>

GUID che specifica un tipo di crittografia supportato.

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

 

 




