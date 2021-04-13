---
description: Contiene un vettore di inizializzazione (IV) per la crittografia a blocchi a 128 bit Advanced Encryption Standard CTR (AES-CTR).
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: Struttura D3DAES_CTR_IV (D3d9types. h)
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
ms.openlocfilehash: 6e0d543fb0e57ae34f181e7ff0f40a1a1f8222b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342541"
---
# <a name="d3daes_ctr_iv-structure"></a>\_Struttura D3DAES CTR \_ IV

Contiene un vettore di inizializzazione (IV) per la crittografia a blocchi a 128 bit Advanced Encryption Standard CTR (AES-CTR).

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

IV, nel formato big-endian.

</dd> <dt>

**Count**
</dt> <dd>

Conteggio dei blocchi, nel formato big-endian.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura **D3DAES \_ CTR \_ IV** e la struttura [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) sono equivalenti.

Per informazioni dettagliate, vedere [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>D3d9types. h (include d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture video Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




