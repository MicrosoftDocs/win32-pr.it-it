---
description: Contiene la risposta a una \_ query D3DAUTHENTICATEDQUERY OUTPUTID.
ms.assetid: 4dfd1d65-b203-456a-bc9b-527906bcf87e
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYROUTPUTID_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 26686126fd2a5cb942c88ea485f753d2432499dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049313"
---
# <a name="d3dauthenticatedchannel_queryroutputid_output-structure"></a>\_Struttura di output QUERYROUTPUTID di D3DAUTHENTICATEDCHANNEL \_

Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) .

Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  HANDLE DeviceHandle;
  HANDLE CryptoSessionHandle;
  UINT   OutputIDIndex;
  UINT64 OutputID;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**\_Output della query D3DAUTHENTICATEDCHANNEL \_**
</dt> <dd>

Struttura [**di \_ \_ output della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (Mac) e altri dati.

</dd> <dt>

**DeviceHandle**
</dt> <dd>

Handle per il dispositivo.

</dd> <dt>

**CryptoSessionHandle**
</dt> <dd>

Handle per la sessione di crittografia.

</dd> <dt>

**OutputIDIndex**
</dt> <dd>

Indice dell'ID di output specificato nel membro **outputID** .

</dd> <dt>

**OutputID**
</dt> <dd>

ID di output associato al dispositivo e alla sessione di crittografia specificati.

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

[**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




