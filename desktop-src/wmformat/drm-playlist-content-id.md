---
title: Struttura DRM_PLAYLIST_CONTENT_ID (Drmexternals. h)
description: La \_ struttura di \_ ID contenuto della playlist DRM \_ contiene informazioni sul contenuto che deve essere copiato su CD come parte di un Burn della playlist.
ms.assetid: 124e86ac-b0d4-40b2-868b-fe2fed1898e1
keywords:
- Formato di Windows Media per la struttura DRM_PLAYLIST_CONTENT_ID
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_PLAYLIST_CONTENT_ID
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f475a8c3620ff1af64cb70914ca1ac591aa55106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302061"
---
# <a name="drm_playlist_content_id-structure"></a>\_Struttura dell' \_ ID contenuto della playlist DRM \_

La struttura di **\_ \_ \_ ID contenuto della playlist DRM** contiene informazioni sul contenuto che deve essere copiato su CD come parte di un Burn della playlist.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_PLAYLIST_CONTENT_ID {
  LPCWSTR lpcwszV2Header;
  LPCSTR  lpcszV1KID;
  BYTE    *pbOtherData;
  DWORD   cbOtherData;
  DWORD   dwUniqueIDForSession;
  DWORD   dwValidFields;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**lpcwszV2Header**
</dt> <dd>

Intestazione DRM. Utilizzare questo membro se il contenuto è protetto da Windows Media DRM versione 2 o successiva.

</dd> <dt>

**lpcszV1KID**
</dt> <dd>

ID chiave Utilizzare questo membro se il contenuto è protetto da Windows Media DRM versione 1.

</dd> <dt>

**pbOtherData**
</dt> <dd>

Buffer contenente dati supplementari.

</dd> <dt>

**cbOtherData**
</dt> <dd>

Dimensioni del buffer **pbOtherData** in byte.

</dd> <dt>

**dwUniqueIDForSession**
</dt> <dd>

Identificatore univoco del contenuto da utilizzare nella sessione corrente.

</dd> <dt>

**dwValidFields**
</dt> <dd>

**DWORD** che indica i campi validi di questa struttura.

</dd> </dl>

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

 

 





