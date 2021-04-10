---
description: 'Contiene i dati di input per il metodo IDirect3DAuthenticatedChannel9:: Configure.'
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
title: Struttura D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 82cd60dbb65517beb65a3a7cb413e1d93ac72062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225822"
---
# <a name="d3dauthenticatedchannel_configure_input-structure"></a>D3DAUTHENTICATEDCHANNEL \_ configurare la \_ struttura di input

Contiene i dati di input per il metodo [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT;
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

Handle per il canale autenticato. Per ottenere l'handle, chiamare [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Numero di sequenza della query. All'inizio della sessione, generare un numero casuale a 32 bit a crittografia sicura da usare come numero di sequenza iniziale. Per ogni comando, incrementare il numero di sequenza di 1.

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

[**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




