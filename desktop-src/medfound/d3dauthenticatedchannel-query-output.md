---
description: 'Contiene la risposta del metodo IDirect3DAuthenticatedChannel9:: query.'
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT (D3d9types. h)
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
ms.openlocfilehash: 79fe02a483ade1ff60107287799624017496887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127935"
---
# <a name="d3dauthenticatedchannel_query_output-structure"></a>Struttura di output della \_ query D3DAUTHENTICATEDCHANNEL \_

Contiene la risposta del metodo [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .

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

**OMAC**
</dt> <dd>

Struttura [**\_ OMAC D3D**](d3d-omac.md) che contiene un Message Authentication Code (Mac) dei dati. Il driver utilizza il MAC CBC a chiave singola (OMAC) basato su AES per calcolare questo valore per il blocco di dati visualizzato dopo questo membro della struttura.

</dd> <dt>

**QueryType**
</dt> <dd>

GUID che specifica la query. Per un elenco di valori, vedere [protezione del contenuto query](content-protection-queries.md).

</dd> <dt>

**GESTIRE**
</dt> <dd>

Handle per il canale autenticato.

</dd> <dt>

**UINT**
</dt> <dd>

Numero di sequenza della query.

</dd> <dt>

**ReturnCode**
</dt> <dd>

Codice risultato per la query.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per i membri **QueryType**, **hChannel** e **SequenceNumber** , il driver usa gli stessi valori forniti dall'applicazione nella struttura di input della [**\_ query D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-input.md) . L'applicazione deve verificare che questi valori corrispondano.

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

 

 




