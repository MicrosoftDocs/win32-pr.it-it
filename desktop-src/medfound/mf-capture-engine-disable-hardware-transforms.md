---
description: Disabilita l'uso di trasformazioni di Media Foundation basate su hardware (MFTs) nel motore di acquisizione.
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: Attributo MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9631804c61fab953793c3f89d1eac3dc2e8f4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309583"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a>\_Attributo di \_ disabilitazione dell'hardware per le \_ \_ \_ trasformazioni MF motore di acquisizione

Disabilita l'uso di trasformazioni di Media Foundation basate su hardware (MFTs) nel motore di acquisizione.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il motore di acquisizione USA decodificatori o codificatori hardware. Per disabilitare l'utilizzo di MFTs hardware, impostare questo attributo su **true** quando si crea il motore di acquisizione.

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

 

 




