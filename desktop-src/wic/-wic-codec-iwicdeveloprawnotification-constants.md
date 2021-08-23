---
description: Flag utilizzati da IWICDevelopRawNotificationCallback per indicare quali membri sono stati modificati.
ms.assetid: 4e94b4f4-abd9-4395-87ec-a08e49a2cf88
title: Costanti IWICDevelopRawNotificationCallback (Wincodec.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885a99ea21ccafdb3961387013d0f6d9f466e48ffe542a3349af7e658b1b1786
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592461"
---
# <a name="iwicdeveloprawnotificationcallback-constants"></a>Costanti IWICDevelopRawNotificationCallback

Flag utilizzati da [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) per indicare quali membri sono stati modificati.



| Costante/valore                                                                                                                                                                                                                                                                                                                                                                                            | Descrizione                                                                                                          |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| <span id="WICRawChangeNotification_ExposureCompensation"></span><span id="wicrawchangenotification_exposurecompensation"></span><span id="WICRAWCHANGENOTIFICATION_EXPOSURECOMPENSATION"></span><dl> <dt>**WICRawChangeNotification \_ ExposureCompensation**</dt> <dt>0x00000001</dt> </dl>             | Maschera usata per segnalare una modifica della compensazione dell'esposizione.<br/>                                                       |
| <span id="WICRawChangeNotification_NamedWhitePoint"></span><span id="wicrawchangenotification_namedwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_NAMEDWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_ NamedWhitePoint**</dt> <dt>0x00000002</dt> </dl>                                 | Maschera usata per segnalare una [**modifica WICNamedWhitePoint.**](/windows/desktop/api/Wincodec/ne-wincodec-wicnamedwhitepoint)<br/>                 |
| <span id="WICRawChangeNotification_KelvinWhitePoint"></span><span id="wicrawchangenotification_kelvinwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_KELVINWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_ KelvinWhitePoint**</dt> <dt>0x00000004</dt> </dl>                             | Maschera usata per segnalare una modifica del punto bianco kelvin.<br/>                                                          |
| <span id="WICRawChangeNotification_RGBWhitePoint"></span><span id="wicrawchangenotification_rgbwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_RGBWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_ RGBWhitePoint**</dt> <dt>0x00000008</dt> </dl>                                         | Maschera usata per segnalare una modifica del punto bianco RGB.<br/>                                                             |
| <span id="WICRawChangeNotification_Contrast"></span><span id="wicrawchangenotification_contrast"></span><span id="WICRAWCHANGENOTIFICATION_CONTRAST"></span><dl> <dt>**WICRawChangeNotification \_ Contrasto**</dt> <dt>0x00000010</dt> </dl>                                                             | Maschera usata per segnalare una modifica del contrasto.<br/>                                                                    |
| <span id="WICRawChangeNotification_Gamma"></span><span id="wicrawchangenotification_gamma"></span><span id="WICRAWCHANGENOTIFICATION_GAMMA"></span><dl> <dt>**WICRawChangeNotification \_ Gamma**</dt> <dt>0x00000020</dt> </dl>                                                                         | Maschera usata per segnalare una modifica gamma.<br/>                                                                       |
| <span id="WICRawChangeNotification_Sharpness"></span><span id="wicrawchangenotification_sharpness"></span><span id="WICRAWCHANGENOTIFICATION_SHARPNESS"></span><dl> <dt>**WICRawChangeNotification \_ Acutità**</dt> <dt>0x00000040</dt> </dl>                                                         | Maschera usata per segnalare una modifica della nitidezza.<br/>                                                                   |
| <span id="WICRawChangeNotification_Saturation"></span><span id="wicrawchangenotification_saturation"></span><span id="WICRAWCHANGENOTIFICATION_SATURATION"></span><dl> <dt>**WICRawChangeNotification \_ Saturazione**</dt> <dt>0x00000080</dt> </dl>                                                     | Maschera usata per segnalare una modifica di saturazione.<br/>                                                                  |
| <span id="WICRawChangeNotification_Tint"></span><span id="wicrawchangenotification_tint"></span><span id="WICRAWCHANGENOTIFICATION_TINT"></span><dl> <dt>**WICRawChangeNotification \_ Tinta**</dt> <dt>0x00000100</dt> </dl>                                                                             | Maschera usata per segnalare una modifica della tinta.<br/>                                                                        |
| <span id="WICRawChangeNotification_NoiseReduction"></span><span id="wicrawchangenotification_noisereduction"></span><span id="WICRAWCHANGENOTIFICATION_NOISEREDUCTION"></span><dl> <dt>**WICRawChangeNotification \_ NoiseReduction**</dt> <dt>0x00000200</dt> </dl>                                     | Maschera usata per segnalare una modifica di riduzione del rumore.<br/>                                                             |
| <span id="WICRawChangeNotification_DestinationColorContext"></span><span id="wicrawchangenotification_destinationcolorcontext"></span><span id="WICRAWCHANGENOTIFICATION_DESTINATIONCOLORCONTEXT"></span><dl> <dt>**WICRawChangeNotification \_ DestinationColorContext**</dt> <dt>0x00000400</dt> </dl> | Maschera usata per segnalare una modifica del contesto del colore di destinazione.<br/>                                                   |
| <span id="WICRawChangeNotification_ToneCurve"></span><span id="wicrawchangenotification_tonecurve"></span><span id="WICRAWCHANGENOTIFICATION_TONECURVE"></span><dl> <dt>**WICRawChangeNotification \_ ToneCurve**</dt> <dt>0x00000800</dt> </dl>                                                         | Maschera usata per segnalare una modifica della curva tonale.<br/>                                                                  |
| <span id="WICRawChangeNotification_Rotation"></span><span id="wicrawchangenotification_rotation"></span><span id="WICRAWCHANGENOTIFICATION_ROTATION"></span><dl> <dt>**WICRawChangeNotification \_ Rotazione**</dt> <dt>0x00001000</dt> </dl>                                                             | Maschera usata per segnalare una [**modifica WICRawRotationCapabilities.**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities)<br/> |
| <span id="WICRawChangeNotification_RenderMode"></span><span id="wicrawchangenotification_rendermode"></span><span id="WICRAWCHANGENOTIFICATION_RENDERMODE"></span><dl> <dt>**WICRawChangeNotification \_ Proprietà RenderMode**</dt> <dt>0x00002000</dt> </dl>                                                     | Maschera usata per segnalare una [**modifica WICRawRenderMode.**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode)<br/>                     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo \[ app desktop di Vista\]<br/>                   |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincodec.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback)
</dt> </dl>

 

 




