---
description: Specifica se il motore di acquisizione usa DirectX Video Acceleration (DXVA) per la decodifica video.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: MF_CAPTURE_ENGINE_DISABLE_DXVA attributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c722b70e1707e6ad5d14b7afca0da2c8d1a63b3a132345e727de1f37023916a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941011"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a>Attributo DISABLE \_ \_ \_ \_ DXVA del MOTORE DI ACQUISIZIONE MF

Specifica se il motore di acquisizione usa DirectX Video Acceleration (DXVA) per la decodifica video.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica se si verificano le condizioni seguenti:

-   Il motore di acquisizione decodifica un flusso video compresso dal dispositivo di acquisizione( ad esempio, se il dispositivo di acquisizione restituisce un video H.264).
-   Il decodificatore video supporta la decodifica con accelerazione hardware tramite DXVA.
-   L'applicazione usa [l'attributo \_ MF CAPTURE \_ ENGINE \_ D3D \_ MANAGER](mf-capture-engine-d3d-manager.md) per impostare Gestione dispositivi DXGI nel motore di acquisizione.

In caso contrario, questo attributo viene ignorato.

Questo attributo consente all'applicazione di disabilitare DXVA durante la decodifica su superfici Direct3D.

Il valore predefinito di questo attributo è **FALSE,** ovvero la decodifica DXVA è abilitata quando disponibile.

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

 

 




