---
description: Contiene la risposta dal metodo IDirect3DAuthenticatedChannel9::Query.
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
title: D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT struttura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2defeaf134db9a2464854554db721586f592fc62110d172e0ac804e010804966
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600831"
---
# <a name="d3dauthenticatedchannel_query_output-structure"></a>Struttura DI OUTPUT DELLE QUERY D3DAUTHENTICATEDCHANNEL \_ \_

Contiene la risposta dal [**metodo IDirect3DAuthenticatedChannel9::Query.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT {
  D3D_OMAC       omac;
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
  HRESULT        ReturnCode;
} D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Omac**
</dt> <dd>

Struttura [**\_ OMAC D3D**](d3d-omac.md) che contiene un Message Authentication Code (MAC) dei dati. Il driver usa CBC MAC (OMAC) basato su AES per calcolare questo valore per il blocco di dati visualizzato dopo questo membro della struttura.

</dd> <dt>

**QueryType**
</dt> <dd>

GUID che specifica la query. Per un elenco di valori, vedere protezione del contenuto [Query](content-protection-queries.md).

</dd> <dt>

**Gestire**
</dt> <dd>

Handle per il canale autenticato.

</dd> <dt>

**Uint**
</dt> <dd>

Numero di sequenza della query.

</dd> <dt>

**ReturnCode**
</dt> <dd>

Codice del risultato per la query.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per i **membri QueryType**, **hChannel** e **SequenceNumber,** il driver usa gli stessi valori forniti dall'applicazione nella struttura [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ INPUT.**](d3dauthenticatedchannel-query-input.md) L'applicazione deve verificare che questi valori corrispondano.

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

 

 




