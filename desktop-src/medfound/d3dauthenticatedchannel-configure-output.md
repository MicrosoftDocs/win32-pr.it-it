---
description: Contiene la risposta a una chiamata al metodo IDirect3DAuthenticatedChannel9::Configure.
ms.assetid: 6f33d3f7-a883-4aca-a058-b656d745f2b1
title: D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT struttura (D3d9types.h)
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
ms.openlocfilehash: a849967e798db0ae0364e843221bfe2bf0f3305f773a784b6330a21bb84e5427
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942931"
---
# <a name="d3dauthenticatedchannel_configure_output-structure"></a>Struttura CONFIGURE OUTPUT di D3DAUTHENTICATEDCHANNEL \_ \_

Contiene la risposta a una chiamata al [**metodo IDirect3DAuthenticatedChannel9::Configure.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)

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

**Omac**
</dt> <dd>

Struttura [**\_ OMAC D3D**](d3d-omac.md) che contiene un Message Authentication Code (MAC) dei dati. Il driver usa OMAC (One-Key CBC MAC) basato su AES per calcolare questo valore per il blocco di dati visualizzato dopo questo membro della struttura.

</dd> <dt>

**ConfigureType**
</dt> <dd>

GUID che specifica il comando. Per un elenco di valori, vedere protezione del contenuto [comandi](content-protection-commands.md).

</dd> <dt>

**hChannel**
</dt> <dd>

Handle per il canale autenticato.

</dd> <dt>

**Sequencenumber**
</dt> <dd>

Numero di sequenza del comando.

</dd> <dt>

**Codice restituito**
</dt> <dd>

Codice del risultato per il comando.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per i **membri ConfigureType**, **hChannel** e **SequenceNumber,** il driver usa gli stessi valori forniti dall'applicazione nella struttura [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT.**](d3dauthenticatedchannel-configure-input.md) L'applicazione deve verificare che questi valori corrispondano.

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

[**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




