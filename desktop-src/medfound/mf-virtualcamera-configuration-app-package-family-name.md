---
description: Specifica il nome della famiglia di pacchetti dell'app per un'applicazione di configurazione della fotocamera virtuale.
title: MF_VIRTUALCAMERA_APP_PACKAGE_FAMILY_NAME attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/24/2021
ms.openlocfilehash: e821a273c44b1d5c9e654e34bbfb928ea707cdc0
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691858"
---
# <a name="mf_virtualcamera_app_package_family_name-attribute"></a><span data-ttu-id="7f103-103">Attributo \_ MF VIRTUALCAMERA \_ APP \_ PACKAGE FAMILY \_ \_ NAME</span><span class="sxs-lookup"><span data-stu-id="7f103-103">MF\_VIRTUALCAMERA\_APP\_PACKAGE\_FAMILY\_NAME attribute</span></span>

<span data-ttu-id="7f103-104">Specifica il nome della famiglia di pacchetti dell'app per un'applicazione di configurazione della fotocamera virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f103-104">Specifies the app package family name for a virtual camera configuration application.</span></span> <span data-ttu-id="7f103-105">Se disponibile, la pipeline associa l'applicazione di configurazione alla fotocamera virtuale e fornisce un punto di lancio all'interno della pagina Impostazioni fotocamera.</span><span class="sxs-lookup"><span data-stu-id="7f103-105">When provided, the pipeline will associate the configuration application with the virtual camera and provide a launch point within the Camera Settings page.</span></span>

## <a name="data-type"></a><span data-ttu-id="7f103-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7f103-106">Data type</span></span>

[<span data-ttu-id="7f103-107">MF_ATTRIBUTE_STRING</span><span class="sxs-lookup"><span data-stu-id="7f103-107">MF_ATTRIBUTE_STRING</span></span>](/windows/win32/api/mfobjects/ne-mfobjects-mf_attribute_type)

## <a name="remarks"></a><span data-ttu-id="7f103-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f103-108">Remarks</span></span>

<span data-ttu-id="7f103-109">Questo attributo può essere esposto dall'origine multimediale personalizzata della fotocamera virtuale dall'archivio attributi di origine multimediale [IMFMediaSourceEx::GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).</span><span class="sxs-lookup"><span data-stu-id="7f103-109">This attribute may be exposed by the virtual camera custom media source from the media source attribute store [IMFMediaSourceEx::GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).</span></span>  

<span data-ttu-id="7f103-110">Se l'applicazione di configurazione non è ancora installata nel computer, l'applicazione Store verrà avviata e passa alla pagina dell'applicazione specificata dal nome della famiglia di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="7f103-110">If the configuration application is not yet installed on the machine, the Store application will be launched and navigated to the application page specified by the package family name.</span></span> <span data-ttu-id="7f103-111">In caso contrario, l'applicazione installata verrà avviata per l'utente.</span><span class="sxs-lookup"><span data-stu-id="7f103-111">Otherwise, the installed application will be launched for the user.</span></span>


## <a name="requirements"></a><span data-ttu-id="7f103-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f103-112">Requirements</span></span>



| <span data-ttu-id="7f103-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f103-113">Requirement</span></span> | <span data-ttu-id="7f103-114">Valore</span><span class="sxs-lookup"><span data-stu-id="7f103-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f103-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f103-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7f103-116">Windows Build 22000</span><span class="sxs-lookup"><span data-stu-id="7f103-116">Windows Build 22000</span></span><br/>                          |
| <span data-ttu-id="7f103-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f103-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7f103-118">Windows Build 22000</span><span class="sxs-lookup"><span data-stu-id="7f103-118">Windows Build 22000</span></span><br/>                      |
| <span data-ttu-id="7f103-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f103-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f103-120"><dt>Mfapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="7f103-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f103-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f103-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f103-122">Elenco alfabetico di Media Foundation attributi</span><span class="sxs-lookup"><span data-stu-id="7f103-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f103-123">**IMFAttributes::GetString**</span><span class="sxs-lookup"><span data-stu-id="7f103-123">**IMFAttributes::GetString**</span></span>](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="7f103-124">**IMFAttributes::SetString**</span><span class="sxs-lookup"><span data-stu-id="7f103-124">**IMFAttributes::SetString**</span></span>](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> 
</dl>
 




