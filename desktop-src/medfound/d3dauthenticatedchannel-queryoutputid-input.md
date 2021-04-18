---
description: Contiene i dati di input per una \_ query OUTPUTID D3DAUTHENTICATEDQUERY.
ms.assetid: 8864c298-be9a-4ff4-a9c5-996b62937c18
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7c64d43261ccc849772372110ad73169c698cd0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305441"
---
# <a name="d3dauthenticatedchannel_queryoutputid_input-structure"></a>\_Struttura di input QUERYOUTPUTID di D3DAUTHENTICATEDCHANNEL \_

Contiene i dati di input per una query [**\_ OUTPUTID D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-outputid.md) .

Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
  UINT                                OutputIDIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Input**
</dt> <dd>

Struttura [**di \_ \_ input della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) che contiene il GUID per la query e altri dati.

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

Indice dell'ID di output.

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

 

 




