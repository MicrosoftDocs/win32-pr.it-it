---
description: Contiene informazioni sul formato per la ricompressione intelligente.
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: Struttura SCompFmt0 (qedit. h)
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
ms.openlocfilehash: ad5a5277718e8d414d64a86b9c31739cf576736a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328150"
---
# <a name="scompfmt0-structure"></a>Struttura SCompFmt0

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

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

Riservati deve essere zero.

</dd> <dt>

**MediaType**
</dt> <dd>

[**Am \_ Struttura del \_ tipo di supporto**](/windows/win32/api/strmif/ns-strmif-am_media_type) che descrive il formato di compressione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAMTimelineGroup::GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




