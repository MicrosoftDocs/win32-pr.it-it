---
description: L'enumerazione TIMELINE \_ MAJOR TYPE specifica il tipo principale di un \_ oggetto.
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: TIMELINE_MAJOR_TYPE enumerazione (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TIMELINE_MAJOR_TYPE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: b18088a9d01b263c80a4ff941a6b7720043da708eaeaebf4f79a2084d1ed258f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501721"
---
# <a name="timeline_major_type-enumeration"></a>Enumerazione TIMELINE \_ MAJOR \_ TYPE

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`TIMELINE_MAJOR_TYPE`L'enumerazione specifica il tipo principale di un oggetto.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  TIMELINE_MAJOR_TYPE_COMPOSITE   = 1,
  TIMELINE_MAJOR_TYPE_TRACK       = 2,
  TIMELINE_MAJOR_TYPE_SOURCE      = 4,
  TIMELINE_MAJOR_TYPE_TRANSITION  = 8,
  TIMELINE_MAJOR_TYPE_EFFECT      = 16,
  TIMELINE_MAJOR_TYPE_GROUP       = 128
} TIMELINE_MAJOR_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**TIPO PRINCIPALE \_ SEQUENZA \_ TEMPORALE \_ COMPOSITO**
</dt> <dd>

Oggetto composito. Contiene una o più tracce.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**TRACCIA \_ DEL TIPO PRINCIPALE DELLA SEQUENZA \_ \_ TEMPORALE**
</dt> <dd>

Oggetto Track. Contiene una o più origini.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**ORIGINE \_ TIPO PRINCIPALE SEQUENZA \_ \_ TEMPORALE**
</dt> <dd>

Oggetto di origine. Contiene un riferimento a un'origine multimediale.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**TRANSIZIONE \_ DEL TIPO PRINCIPALE DELLA SEQUENZA \_ \_ TEMPORALE**
</dt> <dd>

Oggetto Transition. Definisce una transizione tra compositi, tracce o origini.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**EFFETTO TIPO \_ \_ PRINCIPALE SEQUENZA \_ TEMPORALE**
</dt> <dd>

Oggetto Effect. Definisce un effetto a input singolo da applicare a un oggetto composito, di traccia o di origine.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**GRUPPO \_ TIPO PRINCIPALE SEQUENZA \_ \_ TEMPORALE**
</dt> <dd>

Oggetto Group. Contiene una o più tracce di un determinato tipo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAMTimeline**](iamtimeline.md)
</dt> <dt>

[**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[**IAMTimelineObj::GetTimelineType**](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




