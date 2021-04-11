---
description: Imposta un puntatore al Gestione dispositivi DXGI nel motore di acquisizione.
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: Attributo MF_CAPTURE_ENGINE_D3D_MANAGER (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c5e87d4817f539f91ecd55aec10a2086afeaeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129799"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a>\_ \_ \_ Attributo gestione D3D del motore di acquisizione MF \_

Imposta un puntatore al Gestione dispositivi DXGI nel motore di acquisizione.

## <a name="data-type"></a>Tipo di dati

**IUnknown \** _

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un puntatore all'interfaccia [_ *IMFDXGIDeviceManager* *](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) . Questo attributo consente al motore di acquisizione di allocare i fotogrammi video usando le superfici DXGI e di usare l'accelerazione hardware per la decodifica e l'elaborazione video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del motore di acquisizione](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




