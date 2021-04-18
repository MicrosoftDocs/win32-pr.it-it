---
description: Specifica che il codificatore MFT supporta la ricezione di eventi MEEncodingParameter durante il flusso.
ms.assetid: 8DE04537-641C-4154-9C7F-A7D025CA4C39
title: Attributo MFT_ENCODER_SUPPORTS_CONFIG_EVENT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49c688abc4d372a463115c369e4616babe3bcaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310224"
---
# <a name="mft_encoder_supports_config_event-attribute"></a>Il \_ codificatore MFT \_ supporta l' \_ attributo dell' \_ evento config

Specifica che il codificatore MFT supporta la ricezione di eventi [MEEncodingParameter](meencodingparameters.md) durante il flusso.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Inviato dal codificatore MFT tramite [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Mftransform. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFTransform::P rocessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
</dt> </dl>

 

 




