---
description: Contiene un vettore di inizializzazione (IV) per la crittografia a blocchi Advanced Encryption Standard CTR (AES-CTR) a 128 bit.
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: D3DAES_CTR_IV struttura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAES_CTR_IV
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 09535b432ff1af60ad33b622810d0d8a4d190cb81650214aa71b445ba3c22f4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974790"
---
# <a name="d3daes_ctr_iv-structure"></a>Struttura IV CTR D3DAES \_ \_

Contiene un vettore di inizializzazione (IV) per la crittografia a blocchi Advanced Encryption Standard CTR (AES-CTR) a 128 bit.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DAES_CTR_IV {
  UINT64 IV;
  UINT64 Count;
} D3DAES_CTR_IV;
```



## <a name="members"></a>Members

<dl> <dt>

**IV**
</dt> <dd>

Vettore di inizializzazione, in formato big-endian.

</dd> <dt>

**Count**
</dt> <dd>

Conteggio dei blocchi, in formato big-endian.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura IV di \_ CTR D3DAES \_** e la [**struttura IV \_ \_ CTR \_ DXVA2 AES**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) sono equivalenti.

Per informazioni dettagliate, vedere [**DXVA2 \_ AES \_ CTR \_ IV.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>D3d9types.h (includere D3d9.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture video Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




