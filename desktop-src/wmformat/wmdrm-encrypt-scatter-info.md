---
title: WMDRM_ENCRYPT_SCATTER_INFO struttura (Wmdrmsdk.h)
description: La struttura WMDRM ENCRYPT SCATTER INFO contiene le informazioni necessarie \_ \_ per configurare \_ l'interfaccia IWMDRMEncryptScatter per l'uso.
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- WMDRM_ENCRYPT_SCATTER_INFO struttura windows Media Format
- struttura windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_INFO
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef766f40742713b01648348bedb4c1a35494fdc02d02843f8f2a41f133938a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083815"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a>Struttura WMDRM \_ ENCRYPT \_ SCATTER \_ INFO

La **struttura WMDRM \_ ENCRYPT SCATTER \_ \_ INFO** contiene le informazioni necessarie per configurare l'interfaccia [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) per l'uso.

## <a name="syntax"></a>Sintassi


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_INFO {
  DWORD dwStreamID;
  DWORD dwSampleProtectionVersion;
  DWORD cbProtectionInfo;
  BYTE  *pbProtectionInfo;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**dwStreamID**
</dt> <dd>

Identificatore del flusso da crittografare.

</dd> <dt>

**dwSampleProtectionVersion**
</dt> <dd>

Versione di protezione di esempio da usare per codificare i dati dal flusso specificato.

</dd> <dt>

**cbProtectionInfo**
</dt> <dd>

Dimensioni del buffer **pbProtectionInfo** in byte.

</dd> <dt>

**pbProtectionInfo**
</dt> <dd>

Buffer contenente informazioni di protezione aggiuntive.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata dal [**metodo IWMDRMEncryptScatter::InitEncryptScatter.**](iwmdrmencryptscatter-initencryptscatter.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





