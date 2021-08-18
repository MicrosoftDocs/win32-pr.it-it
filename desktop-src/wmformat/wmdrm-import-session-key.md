---
title: WMDRM_IMPORT_SESSION_KEY struttura (Drmexternals.h)
description: La struttura WMDRM \_ IMPORT SESSION KEY contiene la chiave di sessione per \_ \_ l'importazione di contenuto protetto.
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- WMDRM_IMPORT_SESSION_KEY struttura windows Media Format
- Struttura windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_SESSION_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34cdff6d17ad6ce60dd40478b56c9718be0863295422d2e5c60fee2c437dc6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844060"
---
# <a name="wmdrm_import_session_key-structure"></a>Struttura WMDRM \_ IMPORT \_ SESSION \_ KEY

La **struttura WMDRM \_ IMPORT SESSION \_ \_ KEY** contiene la chiave di sessione per l'importazione di contenuto protetto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct WMDRM_IMPORT_SESSION_KEY {
  DWORD dwKeyType;
  DWORD cbKey;
  BYTE  rgbKey[1];
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**dwKeyType**
</dt> <dd>

Tipo di chiave di sessione. Impostare su WMDRM \_ KEYTYPE \_ RC4.

</dd> <dt>

**cbKey**
</dt> <dd>

Dimensioni della chiave di sessione, in byte. Questo valore può essere grande quanto necessario, dati i limiti di una singola operazione OAEP RSA sull'intero messaggio (questa struttura e la chiave di sessione).

</dd> <dt>

**rgbKey**
</dt> <dd>

Indirizzo di un buffer contenente la chiave di sessione. Le dimensioni del buffer devono corrispondere al valore **di cbKey**. I dati nel buffer sono un valore di chiave generato in modo casuale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura, incluso il buffer contenente la chiave di sessione, deve essere crittografata con la chiave pubblica del computer Windows Media DRM e inclusa nel membro **pbEncryptedSessionKeyMessage** della struttura [**WMDRM \_ IMPORT \_ INIT \_ STRUCT.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                      |
| Versione<br/>                  | Windows Media Format 11 SDK<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





