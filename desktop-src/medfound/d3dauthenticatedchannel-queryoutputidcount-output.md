---
description: Contiene la risposta a una query D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT.
ms.assetid: 8b9fa0dc-bbe5-4382-8acc-59aeadfca825
title: D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT struttura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: c97f55d05aff3feb1857456ec04c4fa48872487decc5812912081b894896dce2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777551"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_output-structure"></a>Struttura DI \_ OUTPUT QUERYOUTPUTIDCOUNT D3DAUTHENTICATEDCHANNEL \_

Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT.**](d3dauthenticatedquery-outputidcount.md)

Per inviare questa query, [**chiamare IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
  HANDLE                               CryptoSessionHandle;
  UINT                                 NumOutputIDs;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Output**
</dt> <dd>

Struttura [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ OUTPUT**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (MAC) e altri dati.

</dd> <dt>

**DeviceHandle**
</dt> <dd>

Handle per il dispositivo.

</dd> <dt>

**CryptoSessionHandle**
</dt> <dd>

Handle per la sessione di crittografia.

</dd> <dt>

**NumOutputID**
</dt> <dd>

Numero di ID di output associati al dispositivo e alla sessione di crittografia specificati.

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

 

 




