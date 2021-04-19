---
description: Il \_ \_ tipo di enumerazione dei tipi di dispositivi WPD descrive i diversi tipi di dispositivi portatili Windows (WPD) usati comunemente per determinare la classificazione di base e l'aspetto visivo di un dispositivo portatile.
ms.assetid: 51714e0f-e9b7-4474-a8bb-da3875ef5399
title: Enumerazione WPD_DEVICE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3e71acf200a95bba05b7298a5824bfa353e4a90b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324206"
---
# <a name="wpd_device_types-enumeration"></a><span data-ttu-id="d0158-103">Enumerazione dei tipi di \_ dispositivi WPD \_</span><span class="sxs-lookup"><span data-stu-id="d0158-103">WPD\_DEVICE\_TYPES enumeration</span></span>

<span data-ttu-id="d0158-104">Il tipo di enumerazione dei **\_ \_ tipi di dispositivi WPD** descrive i diversi tipi di dispositivi portatili Windows (WPD) usati comunemente per determinare la classificazione di base e l'aspetto visivo di un dispositivo portatile.</span><span class="sxs-lookup"><span data-stu-id="d0158-104">The **WPD\_DEVICE\_TYPES** enumeration type describes the different Windows Portable Device (WPD) types commonly used to determine the basic classification and visual appearance of a portable device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0158-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0158-105">Syntax</span></span>


```C++
typedef enum tagWPD_DEVICE_TYPES { 
  WPD_DEVICE_TYPE_GENERIC                       = 0,
  WPD_DEVICE_TYPE_CAMERA                        = 1,
  WPD_DEVICE_TYPE_MEDIA_PLAYER                  = 2,
  WPD_DEVICE_TYPE_PHONE                         = 3,
  WPD_DEVICE_TYPE_VIDEO                         = 4,
  WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER  = 5,
  WPD_DEVICE_TYPE_AUDIO_RECORDER                = 6
} WPD_DEVICE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="d0158-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="d0158-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d0158-107"><span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**\_tipo di dispositivo WPD \_ \_ generico**</span><span class="sxs-lookup"><span data-stu-id="d0158-107"><span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**WPD\_DEVICE\_TYPE\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="d0158-108">WPD generico che include dispositivi multifunzione che non rientrano in uno degli altri valori di enumerazione dei [**\_ \_ tipi di dispositivo WPD**](wpd-device-types.md) .</span><span class="sxs-lookup"><span data-stu-id="d0158-108">A generic WPD that includes multifunction devices that do not fall into one of the other [**WPD\_DEVICE\_TYPES**](wpd-device-types.md) enumeration values.</span></span>

</dd> <dt>

<span data-ttu-id="d0158-109"><span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**\_fotocamera del \_ tipo di dispositivo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d0158-109"><span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**WPD\_DEVICE\_TYPE\_CAMERA**</span></span>
</dt> <dd>

<span data-ttu-id="d0158-110">Un dispositivo della fotocamera, ad esempio una fotocamera digitale ancora.</span><span class="sxs-lookup"><span data-stu-id="d0158-110">A camera device, such as a digital still camera.</span></span>

</dd> <dt>

<span data-ttu-id="d0158-111"><span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**\_ \_ \_ media \_ Player tipo di dispositivo WPD**</span><span class="sxs-lookup"><span data-stu-id="d0158-111"><span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER**</span></span>
</dt> <dd>

<span data-ttu-id="d0158-112">Dispositivo multimediale che supporta la riproduzione di immagini audio, video o di visualizzazione, ad esempio un lettore musicale portatile o un Media Center portatile.</span><span class="sxs-lookup"><span data-stu-id="d0158-112">A media player device that supports playing audio, video, or viewing pictures, such as a portable music player or portable media center.</span></span> <span data-ttu-id="d0158-113">Non tutte queste funzioni sono classificate come un tipo di \_ dispositivo \_ WPD \_ media \_ Player.</span><span class="sxs-lookup"><span data-stu-id="d0158-113">Not all of this functionally is classified as a WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER.</span></span> <span data-ttu-id="d0158-114">I dispositivi portatili Music Player, ad esempio, vengono classificati come \_ tipo di dispositivo WPD \_ \_ media \_ Player.</span><span class="sxs-lookup"><span data-stu-id="d0158-114">For example, portable music player devices are classified as WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER.</span></span>

</dd> <dt>

<span data-ttu-id="d0158-115"><span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**\_ \_ telefono tipo di dispositivo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d0158-115"><span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**WPD\_DEVICE\_TYPE\_PHONE**</span></span>
</dt> <dd>

<span data-ttu-id="d0158-116">Un dispositivo telefonico, ad esempio un telefono cellulare.</span><span class="sxs-lookup"><span data-stu-id="d0158-116">A phone device, such as a mobile phone.</span></span>

</dd> <dt>

<span data-ttu-id="d0158-117"><span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**\_video del \_ tipo di dispositivo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d0158-117"><span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**WPD\_DEVICE\_TYPE\_VIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="d0158-118">Un dispositivo video.</span><span class="sxs-lookup"><span data-stu-id="d0158-118">A video device.</span></span>

</dd> <dt>

<span data-ttu-id="d0158-119"><span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**\_ \_ \_ \_ Gestione informazioni personali del tipo di dispositivo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d0158-119"><span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**WPD\_DEVICE\_TYPE\_PERSONAL\_INFORMATION\_MANAGER**</span></span>
</dt> <dd>

<span data-ttu-id="d0158-120">Un dispositivo Personal Information Manager.</span><span class="sxs-lookup"><span data-stu-id="d0158-120">A personal information manager device.</span></span>

</dd> <dt>

<span data-ttu-id="d0158-121"><span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**\_ \_ registratore audio del tipo di dispositivo \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d0158-121"><span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**WPD\_DEVICE\_TYPE\_AUDIO\_RECORDER**</span></span>
</dt> <dd>

<span data-ttu-id="d0158-122">Un dispositivo registratore audio.</span><span class="sxs-lookup"><span data-stu-id="d0158-122">An audio recorder device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0158-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0158-123">Remarks</span></span>

<span data-ttu-id="d0158-124">**WPD \_ I \_ tipi di dispositivo** vengono letti usando l'interfaccia [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="d0158-124">**WPD\_DEVICE\_TYPES** are read using the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface.</span></span> <span data-ttu-id="d0158-125">Le applicazioni WPD possono usare questi valori per determinare l'aspetto visivo generico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0158-125">WPD applications may use these values to determine the generic visual appearance of the device.</span></span> <span data-ttu-id="d0158-126">Ovvero viene visualizzata un'immagine della fotocamera per i dispositivi di tipo fotocamera, viene visualizzata un'immagine del telefono cellulare per i dispositivi simili al telefono e così via.</span><span class="sxs-lookup"><span data-stu-id="d0158-126">That is, a camera picture is displayed for camera-like devices, a mobile phone picture is displayed for phone-like devices, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="d0158-127">Le applicazioni WPD devono usare le funzionalità del dispositivo portatile per determinare la funzione, non il valore dei **\_ \_ tipi di dispositivo WPD** .</span><span class="sxs-lookup"><span data-stu-id="d0158-127">WPD applications must use the capabilities of the portable device to determine functionally, not the **WPD\_DEVICE\_TYPES** value.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d0158-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0158-128">Requirements</span></span>



| <span data-ttu-id="d0158-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0158-129">Requirement</span></span> | <span data-ttu-id="d0158-130">Valore</span><span class="sxs-lookup"><span data-stu-id="d0158-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0158-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0158-131">Header</span></span><br/> | <dl> <span data-ttu-id="d0158-132"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0158-132"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0158-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0158-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0158-134">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="d0158-134">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




