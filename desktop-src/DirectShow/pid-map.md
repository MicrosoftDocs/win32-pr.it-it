---
description: La \_ struttura della mappa PID contiene identifica il contenuto di un ID pacchetto del flusso di trasporto MPEG-2.
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: Struttura PID_MAP (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PID_MAP
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 98b238c61ccfcfb93e4ddcc0a051d9084228f604
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332184"
---
# <a name="pid_map-structure"></a>\_Struttura mappa PID

La `PID_MAP` struttura contiene identifica il contenuto di un ID pacchetto del flusso di trasporto MPEG-2.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  ULONG                ulPID;
  MEDIA_SAMPLE_CONTENT MediaSampleContent;
} PID_MAP;
```



## <a name="members"></a>Members

<dl> <dt>

**ulPID**
</dt> <dd>

Specifica l'ID pacchetto (PID)

</dd> <dt>

**MediaSampleContent**
</dt> <dd>

Specifica il contenuto del payload del pacchetto, come tipo di enumerazione del [**\_ \_ contenuto di esempio multimediale**](media-sample-content.md) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Bdatypes. h (include Bdaiface. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture DirectShow](directshow-structures.md)
</dt> <dt>

[**Interfaccia IEnumPIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




