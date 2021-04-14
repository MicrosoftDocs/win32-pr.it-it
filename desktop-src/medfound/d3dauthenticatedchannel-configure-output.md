---
description: 'Contiene la risposta a una chiamata al metodo IDirect3DAuthenticatedChannel9:: Configure.'
ms.assetid: 6f33d3f7-a883-4aca-a058-b656d745f2b1
title: Struttura D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c7a029bd73069795b83b0b2a330835782192683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342536"
---
# <a name="d3dauthenticatedchannel_configure_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ configurare la \_ struttura di output

Contiene la risposta a una chiamata al metodo [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
  HRESULT  ReturnCode;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**OMAC**
</dt> <dd>

Struttura [**\_ OMAC D3D**](d3d-omac.md) che contiene un Message Authentication Code (Mac) dei dati. Il driver utilizza il MAC CBC a chiave singola (OMAC) basato su AES per calcolare questo valore per il blocco di dati visualizzato dopo questo membro della struttura.

</dd> <dt>

**ConfigureType**
</dt> <dd>

GUID che specifica il comando. Per un elenco di valori, vedere [protezione del contenuto comandi](content-protection-commands.md).

</dd> <dt>

**hChannel**
</dt> <dd>

Handle per il canale autenticato.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Numero di sequenza del comando.

</dd> <dt>

**ReturnCode**
</dt> <dd>

Codice risultato per il comando.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per i membri **ConfigureType**, **hChannel** e **SequenceNumber** , il driver usa gli stessi valori forniti dall'applicazione in D3DAUTHENTICATEDCHANNEL configurare la struttura di [**\_ \_ input**](d3dauthenticatedchannel-configure-input.md) . L'applicazione deve verificare che questi valori corrispondano.

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

[**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




