---
description: L' \_ enumerazione del \_ tipo principale della sequenza temporale specifica il tipo principale di un oggetto.
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: Enumerazione TIMELINE_MAJOR_TYPE (qedit. h)
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
ms.openlocfilehash: 25c3e829aa73d1da78c110ffd148fb0ebaaebdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325470"
---
# <a name="timeline_major_type-enumeration"></a>\_Enumerazione del tipo principale della sequenza temporale \_

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `TIMELINE_MAJOR_TYPE` enumerazione specifica il tipo principale di un oggetto.

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

<span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**\_tipo principale sequenza temporale \_ \_ composita**
</dt> <dd>

Oggetto composito. Include una o più tracce.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**\_traccia del \_ tipo \_ principale della sequenza temporale**
</dt> <dd>

Oggetto Track. Include una o più origini.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**\_ \_ origine tipo principale sequenza temporale \_**
</dt> <dd>

Oggetto di origine. Contiene un riferimento a un'origine multimediale.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**\_transizione di \_ tipo \_ principale della sequenza temporale**
</dt> <dd>

Oggetto di transizione. Definisce una transizione tra compositi, tracce o origini.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**\_effetto del \_ tipo \_ principale della sequenza temporale**
</dt> <dd>

Oggetto effetto. Definisce un effetto a input singolo da applicare a un oggetto composito, di traccia o di origine.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**\_gruppo di \_ tipi \_ principali della sequenza temporale**
</dt> <dd>

Oggetto gruppo. Contiene una o più tracce di un determinato tipo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAMTimeline**](iamtimeline.md)
</dt> <dt>

[**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[**IAMTimelineObj::GetTimelineType**](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




