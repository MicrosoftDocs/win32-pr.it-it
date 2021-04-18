---
description: Definisce gli algoritmi per il processore video usato dall' \_ algoritmo MF video \_ Processor \_ .
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: Enumerazione MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
api_type:
- HeaderDef
api_location:
- mfidl.h
ms.openlocfilehash: 604fee61ae4b6a34d876de8c2863ee6dddad73d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308424"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a>\_Enumerazione del \_ \_ tipo di algoritmo MF Video Processor \_

Definisce gli algoritmi per il processore video usato dall' [ \_ \_ \_ algoritmo MF video processor](mf-video-processor-algorithm.md).

## <a name="syntax"></a>Sintassi


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**\_ \_ \_ impostazione predefinita algoritmo MF Video Processor \_**
</dt> <dd>

la modalità predefinita predilige un equilibrio tra qualità e velocità

</dd> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**\_Algoritmo MF video \_ Processor \_ \_ MRF \_ CRF \_ 444**
</dt> <dd>

Il processore video viene sempre elaborato internamente in AYUV e utilizza filtri di alta qualità.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                              |
| IDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni di Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




