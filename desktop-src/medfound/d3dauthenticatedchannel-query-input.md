---
description: 'Contiene i dati di input per il metodo IDirect3DAuthenticatedChannel9:: query.'
ms.assetid: 6a484652-8da2-4074-96b2-6fe49f4d4200
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERY_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a0bec356b20569b5638848407eff27e930ef76b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225820"
---
# <a name="d3dauthenticatedchannel_query_input-structure"></a>Struttura di input della \_ query D3DAUTHENTICATEDCHANNEL \_

Contiene i dati di input per il metodo [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_INPUT {
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
} D3DAUTHENTICATEDCHANNEL_QUERY_INPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**QueryType**
</dt> <dd>

GUID che specifica la query. Per un elenco di valori, vedere [protezione del contenuto query](content-protection-queries.md).

</dd> <dt>

**GESTIRE**
</dt> <dd>

Handle per il canale autenticato. Per ottenere l'handle, chiamare [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).

</dd> <dt>

**UINT**
</dt> <dd>

Numero di sequenza della query. All'inizio della sessione, generare un numero casuale a 32 bit a crittografia sicura da usare come numero di sequenza iniziale. Per ogni query, incrementare il numero di sequenza di 1.

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

 

 




