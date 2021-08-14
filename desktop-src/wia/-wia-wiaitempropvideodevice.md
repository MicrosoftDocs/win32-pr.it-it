---
description: Il driver video Windows WIA (wiavusd.dll Image Acquisition) standard supporta le proprietà seguenti per i dispositivi video in streaming.
ms.assetid: 24fa7e02-c409-49ec-b1a9-309f7c95e292
title: Costanti delle proprietà del dispositivo WIA video (Wiadef.h)
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
ms.openlocfilehash: 9652ac72d6e73a9c44d2f4b299823dad9cc566bb1c7c0129af497ea213a6e5d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207369"
---
# <a name="video-wia-device-property-constants"></a>Costanti delle proprietà del dispositivo WIA video

Il driver video Windows WIA (wiavusd.dll Image Acquisition) standard supporta le proprietà seguenti per i dispositivi video in streaming.

> [!Note]  
> WIA non supporta i dispositivi video in Windows Server 2003, Windows Vista o versioni successive. Per queste versioni del Windows, [usare](/previous-versions//ms783323(v=vs.85)) DirectShow per acquisire immagini dal video.

 

Il prefisso "WIA DPV" indica una proprietà del dispositivo per i dispositivi video ed è la convenzione di denominazione usata \_ \_ in C/C++. A scopo di scripting, queste costanti usano il prefisso "VideoDevice" e fanno parte del tipo enumerato [WiaItemPropertyId.](-wia-wiaitempropertyid.md) Il nome del membro corrispondente dell'enumerazione di script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.



| Costante/valore                                                                                                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <dt>**WIA \_ DPV \_ LAST \_ PICTURE \_ TAKEN**</dt> <dt>VideoDeviceLastPictureTaken</dt> </dl> | Questa proprietà viene usata per notificare al driver WIA che è stata aggiunta una nuova immagine. Le applicazioni devono impostare il valore di questa proprietà sul nome del file di immagine creato come risultato di una chiamata riuscita al metodo [**IWiaVideo::TakePicture.**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) <br/> Tipo: VT \_ BSTR, Accesso: Lettura/Scrittura<br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <dt>**WIA \_ DPV \_ IMAGES \_ DIRECTORY**</dt> <dt>VideoDeviceImagesDirectory</dt> </dl>         | Questa proprietà è esposta dal driver in modalità utente video WIA standard (wiavusd.dll). Il valore di questa proprietà è il percorso completo della directory in cui il driver video WIA inserisce le immagini per impostazione predefinita. Le applicazioni devono impostare [**la proprietà IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) su questo valore. <br/> Tipo: VT \_ BSTR, Accesso: Sola lettura<br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <dt>**WIA \_ DPV \_ DSHOW \_ DEVICE \_ PATH**</dt> <dt>VideoDeviceDShowDevicePath</dt> </dl>     | Percorso completo del dispositivo DirectShow dispositivo. <br/> Tipo: VT \_ BSTR, Accesso: Sola lettura<br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <dt>**WIA \_ DPF \_ MOUNT \_ POINT**</dt> <dt>FileDeviceMountPoint</dt> </dl>                              | Non implementato. <br/> Tipo: **VT \_ I4,** Accesso: Sola lettura, Valori validi: [WIA \_ PROP \_ NONE](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 
