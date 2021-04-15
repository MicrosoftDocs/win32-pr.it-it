---
title: Struttura WMDRM_IMPORT_CONTENT_KEY (Drmexternals. h)
description: La \_ struttura della chiave simmetrica di importazione WMDRM \_ \_ Archivia la chiave simmetrica usata per l'importazione del contenuto protetto.
ms.assetid: 29a0f98d-96a3-46b2-a67c-dbb23449e927
keywords:
- Formato di Windows Media per la struttura WMDRM_IMPORT_CONTENT_KEY
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_CONTENT_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d616cfe856a19f4f8ffa5254254d3946b1544dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400290"
---
# <a name="wmdrm_import_content_key-structure"></a>WMDRM \_ importare \_ la \_ struttura della chiave simmetrica

La struttura della **\_ \_ \_ chiave simmetrica di importazione WMDRM** archivia la chiave simmetrica usata per l'importazione del contenuto protetto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct WMDRM_IMPORT_CONTENT_KEY {
  DWORD dwVersion;
  DWORD cbStructSize;
  DWORD dwIVKeyType;
  DWORD cbIVKey;
  DWORD dwContentKeyType;
  DWORD cbContentKey;
  BYTE  rgbKeyData[1];
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**dwVersion**
</dt> <dd>

Versione.

</dd> <dt>

**cbStructSize**
</dt> <dd>

Dimensione della struttura in byte.

</dd> <dt>

**dwIVKeyType**
</dt> <dd>

Tipo di chiave del vettore di inizializzazione. Impostare su WMDRM di \_ tipo \_ RC4.

</dd> <dt>

**cbIVKey**
</dt> <dd>

Dimensioni in byte della chiave del vettore di inizializzazione.

</dd> <dt>

**dwContentKeyType**
</dt> <dd>

Tipo di chiave simmetrica. Impostare su WMDRM \_ \_ .

</dd> <dt>

**cbContentKey**
</dt> <dd>

Dimensioni in byte della chiave simmetrica.

</dd> <dt>

**rgbKeyData**
</dt> <dd>

Indirizzo di un buffer contenente la chiave simmetrica. Le dimensioni del buffer devono corrispondere al valore di **cbContentKey**. Questa chiave deve corrispondere alla chiave importata dal messaggio di licenza XMR.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura, incluso il buffer contenente la chiave della sessione, deve essere crittografata con la chiave della sessione e inclusa nel membro **pbEncryptedKeyMessage** della struttura dello [**\_ \_ \_ struct di importazione WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .

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

 

 





