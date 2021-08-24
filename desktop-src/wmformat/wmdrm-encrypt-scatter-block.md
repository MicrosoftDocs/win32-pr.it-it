---
title: WMDRM_ENCRYPT_SCATTER_BLOCK (Wmdrmsdk.h)
description: La struttura WMDRM \_ ENCRYPT SCATTER BLOCK contiene un blocco di dati da \_ \_ crittografare.
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- WMDRM_ENCRYPT_SCATTER_BLOCK struttura windows Media Format
- struttura windows Media Format
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
ms.openlocfilehash: 258cb7e0d8d2cac8da40197aaa45028a56af0ff3a313d65c1a98c50d45b8d3b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658161"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a>Struttura DEL BLOCCO A DISPERSIONE WMDRM \_ ENCRYPT \_ \_

La **struttura WMDRM \_ ENCRYPT SCATTER \_ \_ BLOCK** contiene un blocco di dati da crittografare.

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

Dimensione del blocco in byte.

</dd> <dt>

**pbBlock**
</dt> <dd>

Puntatore a un buffer contenente il blocco di dati.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata dal [**metodo IWMDRMEncryptScatter::EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) per identificare i blocchi di dati da crittografare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





