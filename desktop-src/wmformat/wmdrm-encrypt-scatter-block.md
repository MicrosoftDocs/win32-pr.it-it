---
title: Struttura WMDRM_ENCRYPT_SCATTER_BLOCK (wmdrmsdk. h)
description: La \_ \_ struttura di blocco a dispersione crittografata WMDRM \_ contiene un blocco di dati da crittografare.
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- Formato di Windows Media per la struttura WMDRM_ENCRYPT_SCATTER_BLOCK
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_BLOCK
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8911ba1822b146de4a99ff1fe144afcfd8e212e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324817"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a>\_ \_ Struttura blocco a dispersione crittografia WMDRM \_

La struttura di **\_ \_ \_ blocco a dispersione crittografata WMDRM** contiene un blocco di dati da crittografare.

## <a name="syntax"></a>Sintassi


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_BLOCK {
  DWORD dwStreamID;
  DWORD cbBlock;
  BYTE  *pbBlock;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**dwStreamID**
</dt> <dd>

Identificatore del flusso a cui appartiene il blocco di dati.

</dd> <dt>

**cbBlock**
</dt> <dd>

Dimensioni del blocco in byte.

</dd> <dt>

**pbBlock**
</dt> <dd>

Puntatore a un buffer contenente il blocco di dati.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata dal metodo [**IWMDRMEncryptScatter:: EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) per identificare i blocchi di dati da crittografare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





