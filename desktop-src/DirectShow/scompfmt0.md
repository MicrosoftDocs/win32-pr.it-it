---
description: Contiene informazioni sul formato per la ricompressione intelligente.
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: Struttura SCompFmt0 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCompFmt0
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: f02c9cda80acdd42d0687502834a9b2e66f1cf773d02b88eadabdd346850061e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072705"
---
# <a name="scompfmt0-structure"></a>Struttura SCompFmt0

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Contiene informazioni sul formato per la ricompressione intelligente.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SCompFmt0 {
  long          nFormatId;
  AM_MEDIA_TYPE MediaType;
} SCompFmt0;
```



## <a name="members"></a>Members

<dl> <dt>

**nFormatId**
</dt> <dd>

Riservato; deve essere zero.

</dd> <dt>

**MediaType**
</dt> <dd>

[**AM \_ Struttura \_ MEDIA TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) che descrive il formato di compressione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAMTimelineGroup::GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




