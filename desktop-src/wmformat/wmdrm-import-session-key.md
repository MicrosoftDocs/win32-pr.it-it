---
title: Struttura WMDRM_IMPORT_SESSION_KEY (Drmexternals. h)
description: La \_ struttura della \_ chiave della sessione di importazione WMDRM \_ include la chiave della sessione per l'importazione del contenuto protetto.
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- Formato di Windows Media per la struttura WMDRM_IMPORT_SESSION_KEY
- struttura Windows Media Format
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
ms.openlocfilehash: 93295e73e4e3e5e13b438f8b62e0ab6bfff43ee7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120854"
---
# <a name="wmdrm_import_session_key-structure"></a>WMDRM \_ importare \_ la \_ struttura della chiave della sessione

La struttura della **\_ chiave della \_ sessione \_ di importazione WMDRM** include la chiave della sessione per l'importazione del contenuto protetto.

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

Tipo di chiave della sessione. Impostare su WMDRM di \_ tipo \_ RC4.

</dd> <dt>

**cbKey**
</dt> <dd>

Dimensione, in byte, della chiave della sessione. Questo valore può essere il più grande necessario, dati i limiti di una singola operazione RSA OAEP sull'intero messaggio (la struttura più la chiave della sessione).

</dd> <dt>

**rgbKey**
</dt> <dd>

Indirizzo di un buffer contenente la chiave della sessione. Le dimensioni del buffer devono corrispondere al valore di **cbKey**. I dati nel buffer sono un valore di chiave generato in modo casuale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura, incluso il buffer contenente la chiave della sessione, deve essere crittografata con la chiave pubblica del computer DRM di Windows Media e inclusa nel membro **pbEncryptedSessionKeyMessage** della struttura dello [**\_ \_ \_ struct di importazione WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                      |
| Versione<br/>                  | SDK di Windows Media Format 11<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





