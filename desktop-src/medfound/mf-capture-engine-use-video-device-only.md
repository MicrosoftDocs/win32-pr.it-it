---
description: Specifica se il motore di acquisizione acquisisce video ma non audio.
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY attributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd8dd903c4c56b52bf82a97b28edd5148e3c091788376f1ef460047b7f609b51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973970"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a>Attributo USE VIDEO DEVICE ONLY DEL MOTORE \_ \_ \_ DI \_ \_ ACQUISIZIONE \_ MF

Specifica se il motore di acquisizione acquisisce video ma non audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Se questo attributo è **TRUE,** il motore di acquisizione non seleziona né usa un dispositivo di acquisizione audio. Impostare questo attributo su **TRUE se** si vuole acquisire video senza audio. Il valore predefinito è **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                   |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del motore di acquisizione](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




