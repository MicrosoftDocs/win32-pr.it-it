---
description: Il driver video Windows Image Acquisition (WIA) standard (wiavusd.dll) supporta le proprietà seguenti per lo streaming di dispositivi video.
ms.assetid: 24fa7e02-c409-49ec-b1a9-309f7c95e292
title: Costanti della proprietà del dispositivo WIA video (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPV_LAST_PICTURE_TAKEN
- WIA_DPV_IMAGES_DIRECTORY
- WIA_DPV_DSHOW_DEVICE_PATH
- WIA_DPF_MOUNT_POINT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f02991cb5c2b8cc15eb89e335ef1e46442c89510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129375"
---
# <a name="video-wia-device-property-constants"></a>Costanti della proprietà del dispositivo WIA video

Il driver video Windows Image Acquisition (WIA) standard (wiavusd.dll) supporta le proprietà seguenti per lo streaming di dispositivi video.

> [!Note]  
> WIA non supporta i dispositivi video in Windows Server 2003, Windows Vista o versioni successive. Per queste versioni di Windows, usare [DirectShow](/previous-versions//ms783323(v=vs.85)) per acquisire immagini dal video.

 

Il prefisso "WIA \_ DPV \_ " indica una proprietà del dispositivo per i dispositivi video ed è la convenzione di denominazione usata in C/C++. Per finalità di scripting queste costanti usano il prefisso "VideoDevice" e fanno parte del tipo enumerato [WiaItemPropertyId](-wia-wiaitempropertyid.md) . Il nome del membro corrispondente da tale enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.



| Costante/valore                                                                                                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <dt>**WIA \_ DPV \_ Ultima \_ immagine \_ acquisita**</dt> <dt>VideoDeviceLastPictureTaken</dt> </dl> | Questa proprietà viene utilizzata per notificare al driver WIA che è stata aggiunta una nuova immagine. Le applicazioni devono impostare il valore di questa proprietà sul nome del file di immagine creato in seguito a una chiamata riuscita al metodo [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) . <br/> Tipo: VT \_ BSTR, accesso: lettura/scrittura<br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <dt>**WIA \_ \_ \_ Directory immagini DPV**</dt> <dt>VideoDeviceImagesDirectory</dt> </dl>         | Questa proprietà è esposta dal driver in modalità utente video WIA standard (wiavusd.dll). Il valore di questa proprietà è il percorso completo della directory in cui il driver video WIA inserisce le immagini per impostazione predefinita. Le applicazioni devono impostare la proprietà [**IWiaVideo:: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) su questo valore. <br/> Tipo: VT \_ BSTR, accesso: sola lettura<br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <dt>**WIA \_ VideoDeviceDShowDevicePath \_ \_ \_ percorso dispositivo dshow DPV**</dt> <dt></dt> </dl>     | Percorso completo del dispositivo DirectShow. <br/> Tipo: VT \_ BSTR, accesso: sola lettura<br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <dt>**WIA \_ \_ \_ Punto di montaggio DPF**</dt> <dt>FileDeviceMountPoint</dt> </dl>                              | Non implementato. <br/> Tipo: **VT \_ I4**, accesso: sola lettura, valori validi: [WIA \_ prop \_ None](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
