---
description: Definisce gli algoritmi per il processore video che viene utilizzato da MF \_ VIDEO \_ PROCESSOR \_ ALGORITHM.
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: MF_VIDEO_PROCESSOR_ALGORITHM_TYPE enumerazione
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
ms.openlocfilehash: 885c3e9c34fa787a6877fd37eef81f470be395225594b90b2f5516a8e773eb88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244139"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a>Enumerazione MF \_ VIDEO \_ PROCESSOR ALGORITHM \_ \_ TYPE

Definisce gli algoritmi per il processore video che viene utilizzato da [MF \_ VIDEO PROCESSOR \_ \_ ALGORITHM](mf-video-processor-algorithm.md).

## <a name="syntax"></a>Sintassi


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**ALGORITMO DEL PROCESSORE VIDEO MF \_ \_ \_ \_ PREDEFINITO**
</dt> <dd>

la modalità predefinita favorisce un equilibrio tra qualità e velocità

</dd> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**ALGORITMO DEL \_ \_ PROCESSORE VIDEO \_ \_ MF MRF \_ CRF \_ 444**
</dt> <dd>

Il processore video verrà sempre elaborato internamente in AYUV e userà filtri di alta qualità.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                              |
| Idl<br/>                      | <dl> <dt>Mfidl.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[enumerazioni Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




