---
title: Struttura WMDRM_ENCRYPT_SCATTER_INFO (wmdrmsdk. h)
description: La \_ struttura di \_ informazioni per la crittografia a dispersione WMDRM \_ contiene le informazioni necessarie per configurare l'interfaccia IWMDRMEncryptScatter per l'uso.
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- Formato di Windows Media per la struttura WMDRM_ENCRYPT_SCATTER_INFO
- struttura Windows Media Format
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
ms.openlocfilehash: 500012231f6860fd94038b240355eda9aa2aee44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326606"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a>\_Struttura delle \_ informazioni di dispersione di crittografia WMDRM \_

La struttura di informazioni per la **\_ crittografia a \_ dispersione \_ WMDRM** contiene le informazioni necessarie per configurare l'interfaccia [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) per l'uso.

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

Versione di esempio di protezione da usare per codificare i dati dal flusso specificato.

</dd> <dt>

**cbProtectionInfo**
</dt> <dd>

Dimensioni del buffer **pbProtectionInfo** in byte.

</dd> <dt>

**pbProtectionInfo**
</dt> <dd>

Buffer contenente informazioni aggiuntive sulla protezione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata dal metodo [**IWMDRMEncryptScatter:: InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





