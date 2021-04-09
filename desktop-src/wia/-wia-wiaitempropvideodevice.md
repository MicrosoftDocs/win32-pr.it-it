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
# <a name="video-wia-device-property-constants"></a><span data-ttu-id="b656e-103">Costanti della proprietà del dispositivo WIA video</span><span class="sxs-lookup"><span data-stu-id="b656e-103">Video WIA Device Property Constants</span></span>

<span data-ttu-id="b656e-104">Il driver video Windows Image Acquisition (WIA) standard (wiavusd.dll) supporta le proprietà seguenti per lo streaming di dispositivi video.</span><span class="sxs-lookup"><span data-stu-id="b656e-104">The standard Windows Image Acquisition (WIA) video driver (wiavusd.dll) supports the following properties for streaming video devices.</span></span>

> [!Note]  
> <span data-ttu-id="b656e-105">WIA non supporta i dispositivi video in Windows Server 2003, Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b656e-105">WIA does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="b656e-106">Per queste versioni di Windows, usare [DirectShow](/previous-versions//ms783323(v=vs.85)) per acquisire immagini dal video.</span><span class="sxs-lookup"><span data-stu-id="b656e-106">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

<span data-ttu-id="b656e-107">Il prefisso "WIA \_ DPV \_ " indica una proprietà del dispositivo per i dispositivi video ed è la convenzione di denominazione usata in C/C++.</span><span class="sxs-lookup"><span data-stu-id="b656e-107">The prefix "WIA\_DPV\_" indicates a Device Property for Video devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="b656e-108">Per finalità di scripting queste costanti usano il prefisso "VideoDevice" e fanno parte del tipo enumerato [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="b656e-108">For scripting purposes these constants use the prefix "VideoDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="b656e-109">Il nome del membro corrispondente da tale enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="b656e-109">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



| <span data-ttu-id="b656e-110">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="b656e-110">Constant/value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="b656e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b656e-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <span data-ttu-id="b656e-112"><dt>**WIA \_ DPV \_ Ultima \_ immagine \_ acquisita**</dt> <dt>VideoDeviceLastPictureTaken</dt></span><span class="sxs-lookup"><span data-stu-id="b656e-112"><dt>**WIA\_DPV\_LAST\_PICTURE\_TAKEN**</dt> <dt>VideoDeviceLastPictureTaken</dt></span></span> </dl> | <span data-ttu-id="b656e-113">Questa proprietà viene utilizzata per notificare al driver WIA che è stata aggiunta una nuova immagine.</span><span class="sxs-lookup"><span data-stu-id="b656e-113">This property is used to notify the WIA driver that a new image has been added.</span></span> <span data-ttu-id="b656e-114">Le applicazioni devono impostare il valore di questa proprietà sul nome del file di immagine creato in seguito a una chiamata riuscita al metodo [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) .</span><span class="sxs-lookup"><span data-stu-id="b656e-114">Applications should set the value of this property to the name of the image file created as the result of a successful call to the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method.</span></span> <br/> <span data-ttu-id="b656e-115">Tipo: VT \_ BSTR, accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b656e-115">Type: VT\_BSTR, Access: Read/Write</span></span><br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <span data-ttu-id="b656e-116"><dt>**WIA \_ \_ \_ Directory immagini DPV**</dt> <dt>VideoDeviceImagesDirectory</dt></span><span class="sxs-lookup"><span data-stu-id="b656e-116"><dt>**WIA\_DPV\_IMAGES\_DIRECTORY**</dt> <dt>VideoDeviceImagesDirectory</dt></span></span> </dl>         | <span data-ttu-id="b656e-117">Questa proprietà è esposta dal driver in modalità utente video WIA standard (wiavusd.dll).</span><span class="sxs-lookup"><span data-stu-id="b656e-117">This property is exposed by the standard WIA video user-mode driver (wiavusd.dll).</span></span> <span data-ttu-id="b656e-118">Il valore di questa proprietà è il percorso completo della directory in cui il driver video WIA inserisce le immagini per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b656e-118">The value of this property is the full path of the directory where the WIA video driver puts images by default.</span></span> <span data-ttu-id="b656e-119">Le applicazioni devono impostare la proprietà [**IWiaVideo:: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) su questo valore.</span><span class="sxs-lookup"><span data-stu-id="b656e-119">Applications should set the [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) property to this value.</span></span> <br/> <span data-ttu-id="b656e-120">Tipo: VT \_ BSTR, accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b656e-120">Type: VT\_BSTR, Access: Read Only</span></span><br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <span data-ttu-id="b656e-121"><dt>**WIA \_ VideoDeviceDShowDevicePath \_ \_ \_ percorso dispositivo dshow DPV**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b656e-121"><dt>**WIA\_DPV\_DSHOW\_DEVICE\_PATH**</dt> <dt>VideoDeviceDShowDevicePath</dt></span></span> </dl>     | <span data-ttu-id="b656e-122">Percorso completo del dispositivo DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b656e-122">The full path of the DirectShow device.</span></span> <br/> <span data-ttu-id="b656e-123">Tipo: VT \_ BSTR, accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b656e-123">Type: VT\_BSTR, Access: Read Only</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <span data-ttu-id="b656e-124"><dt>**WIA \_ \_ \_ Punto di montaggio DPF**</dt> <dt>FileDeviceMountPoint</dt></span><span class="sxs-lookup"><span data-stu-id="b656e-124"><dt>**WIA\_DPF\_MOUNT\_POINT**</dt> <dt>FileDeviceMountPoint</dt></span></span> </dl>                              | <span data-ttu-id="b656e-125">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="b656e-125">Not implemented.</span></span> <br/> <span data-ttu-id="b656e-126">Tipo: **VT \_ I4**, accesso: sola lettura, valori validi: [WIA \_ prop \_ None](-wia-property-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="b656e-126">Type: **VT\_I4**, Access: Read Only, Valid values: [WIA\_PROP\_NONE](-wia-property-attributes.md)</span></span><br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="b656e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b656e-127">Requirements</span></span>



| <span data-ttu-id="b656e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b656e-128">Requirement</span></span> | <span data-ttu-id="b656e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b656e-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b656e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b656e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b656e-131">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b656e-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b656e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b656e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b656e-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b656e-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b656e-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b656e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b656e-135"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="b656e-135"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
