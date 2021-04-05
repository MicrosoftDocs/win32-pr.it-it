---
description: Flag utilizzati da IWICDevelopRawNotificationCallback per indicare quali membri sono stati modificati.
ms.assetid: 4e94b4f4-abd9-4395-87ec-a08e49a2cf88
title: Costanti IWICDevelopRawNotificationCallback (wincodec. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8bf5d7cb2f4ac0e6fddd1f2e9151c95143b0cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968250"
---
# <a name="iwicdeveloprawnotificationcallback-constants"></a>Costanti IWICDevelopRawNotificationCallback

Flag utilizzati da [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) per indicare quali membri sono stati modificati.



| Costante/valore                                                                                                                                                                                                                                                                                                                                                                                            | Descrizione                                                                                                          |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| <span id="WICRawChangeNotification_ExposureCompensation"></span><span id="wicrawchangenotification_exposurecompensation"></span><span id="WICRAWCHANGENOTIFICATION_EXPOSURECOMPENSATION"></span><dl> <dt>**WICRawChangeNotification \_**</dt> <dt>0x00000001</dt> ExposureCompensation </dl>             | Maschera utilizzata per segnalare una modifica della compensazione dell'esposizione.<br/>                                                       |
| <span id="WICRawChangeNotification_NamedWhitePoint"></span><span id="wicrawchangenotification_namedwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_NAMEDWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_**</dt> <dt>0x00000002</dt> NamedWhitePoint </dl>                                 | Maschera utilizzata per segnalare una modifica [**WICNamedWhitePoint**](/windows/desktop/api/Wincodec/ne-wincodec-wicnamedwhitepoint) .<br/>                 |
| <span id="WICRawChangeNotification_KelvinWhitePoint"></span><span id="wicrawchangenotification_kelvinwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_KELVINWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_**</dt> <dt>0x00000004</dt> KelvinWhitePoint </dl>                             | Maschera utilizzata per segnalare una modifica al punto bianco Kelvin.<br/>                                                          |
| <span id="WICRawChangeNotification_RGBWhitePoint"></span><span id="wicrawchangenotification_rgbwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_RGBWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_**</dt> <dt>0x00000008</dt> RGBWhitePoint </dl>                                         | Maschera utilizzata per segnalare una modifica del punto bianco RGB.<br/>                                                             |
| <span id="WICRawChangeNotification_Contrast"></span><span id="wicrawchangenotification_contrast"></span><span id="WICRAWCHANGENOTIFICATION_CONTRAST"></span><dl> <dt>**WICRawChangeNotification \_ Contrasto**</dt> <dt>0x00000010</dt> </dl>                                                             | Maschera utilizzata per segnalare una modifica al contrasto.<br/>                                                                    |
| <span id="WICRawChangeNotification_Gamma"></span><span id="wicrawchangenotification_gamma"></span><span id="WICRAWCHANGENOTIFICATION_GAMMA"></span><dl> <dt>**WICRawChangeNotification \_**</dt> <dt>0x00000020</dt> gamma </dl>                                                                         | Maschera utilizzata per segnalare una modifica gamma.<br/>                                                                       |
| <span id="WICRawChangeNotification_Sharpness"></span><span id="wicrawchangenotification_sharpness"></span><span id="WICRAWCHANGENOTIFICATION_SHARPNESS"></span><dl> <dt>**WICRawChangeNotification \_ Nitidezza**</dt> <dt>0x00000040</dt> </dl>                                                         | Maschera utilizzata per segnalare una modifica della nitidezza.<br/>                                                                   |
| <span id="WICRawChangeNotification_Saturation"></span><span id="wicrawchangenotification_saturation"></span><span id="WICRAWCHANGENOTIFICATION_SATURATION"></span><dl> <dt>**WICRawChangeNotification \_ Saturazione**</dt> <dt>0x00000080</dt> </dl>                                                     | Maschera utilizzata per segnalare una modifica della saturazione.<br/>                                                                  |
| <span id="WICRawChangeNotification_Tint"></span><span id="wicrawchangenotification_tint"></span><span id="WICRAWCHANGENOTIFICATION_TINT"></span><dl> <dt>**WICRawChangeNotification \_ Tinta**</dt> <dt>0x00000100</dt> </dl>                                                                             | Maschera utilizzata per segnalare una modifica della tinta.<br/>                                                                        |
| <span id="WICRawChangeNotification_NoiseReduction"></span><span id="wicrawchangenotification_noisereduction"></span><span id="WICRAWCHANGENOTIFICATION_NOISEREDUCTION"></span><dl> <dt>**WICRawChangeNotification \_**</dt> <dt>0x00000200</dt> noisereduction </dl>                                     | Maschera utilizzata per segnalare una modifica della riduzione del rumore.<br/>                                                             |
| <span id="WICRawChangeNotification_DestinationColorContext"></span><span id="wicrawchangenotification_destinationcolorcontext"></span><span id="WICRAWCHANGENOTIFICATION_DESTINATIONCOLORCONTEXT"></span><dl> <dt>**WICRawChangeNotification \_**</dt> <dt>0x00000400</dt> DestinationColorContext </dl> | Maschera utilizzata per segnalare una modifica del contesto del colore di destinazione.<br/>                                                   |
| <span id="WICRawChangeNotification_ToneCurve"></span><span id="wicrawchangenotification_tonecurve"></span><span id="WICRAWCHANGENOTIFICATION_TONECURVE"></span><dl> <dt>**WICRawChangeNotification \_**</dt> <dt>0x00000800</dt> ToneCurve </dl>                                                         | Maschera utilizzata per segnalare una variazione della curva di tono.<br/>                                                                  |
| <span id="WICRawChangeNotification_Rotation"></span><span id="wicrawchangenotification_rotation"></span><span id="WICRAWCHANGENOTIFICATION_ROTATION"></span><dl> <dt>**WICRawChangeNotification \_**</dt> <dt>0x00001000</dt> rotazione </dl>                                                             | Maschera utilizzata per segnalare una modifica [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) .<br/> |
| <span id="WICRawChangeNotification_RenderMode"></span><span id="wicrawchangenotification_rendermode"></span><span id="WICRAWCHANGENOTIFICATION_RENDERMODE"></span><dl> <dt>**WICRawChangeNotification \_**</dt> <dt>0x00002000</dt> RenderMode </dl>                                                     | Maschera utilizzata per segnalare una modifica [**WICRawRenderMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) .<br/>                     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, \[ solo app desktop di Windows Vista\]<br/>                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincodec. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback)
</dt> </dl>

 

 




