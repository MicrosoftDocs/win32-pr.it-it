---
description: 'Altre informazioni su: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION'
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561a348588b1244a6763eb447affa2b330e9c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527883"
---
# <a name="opm_get_connected_hdcp_device_information"></a><span data-ttu-id="ba838-103">\_ \_ \_ \_ informazioni sul dispositivo HDCP connesso \_ ad OPM</span><span class="sxs-lookup"><span data-stu-id="ba838-103">OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION</span></span>

<span data-ttu-id="ba838-104">Ottiene informazioni su un dispositivo High-Bandwidth Digital protezione del contenuto (HDCP) collegato all'output del video.</span><span class="sxs-lookup"><span data-stu-id="ba838-104">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="ba838-105">Vengono restituite le seguenti informazioni:</span><span class="sxs-lookup"><span data-stu-id="ba838-105">The following information is returned:</span></span>

-   <span data-ttu-id="ba838-106">Il vettore di selezione della chiave HDCP del dispositivo (KSV).</span><span class="sxs-lookup"><span data-stu-id="ba838-106">The device's HDCP key selection vector (KSV).</span></span>
-   <span data-ttu-id="ba838-107">Indica se il dispositivo è un ripetitore HDCP.</span><span class="sxs-lookup"><span data-stu-id="ba838-107">Whether the device is an HDCP repeater.</span></span>



| <span data-ttu-id="ba838-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba838-108">Requirement</span></span> | <span data-ttu-id="ba838-109">Valore</span><span class="sxs-lookup"><span data-stu-id="ba838-109">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba838-110">GUID richiesta</span><span class="sxs-lookup"><span data-stu-id="ba838-110">Request GUID</span></span> | <span data-ttu-id="ba838-111">\_ \_ \_ \_ informazioni sul dispositivo HDCP connesso \_ ad OPM</span><span class="sxs-lookup"><span data-stu-id="ba838-111">OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION</span></span>                                                          |
| <span data-ttu-id="ba838-112">Dati di input</span><span class="sxs-lookup"><span data-stu-id="ba838-112">Input data</span></span>   | <span data-ttu-id="ba838-113">nessuno</span><span class="sxs-lookup"><span data-stu-id="ba838-113">None</span></span>                                                                                                    |
| <span data-ttu-id="ba838-114">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="ba838-114">Return data</span></span>  | <span data-ttu-id="ba838-115">Struttura [**di \_ \_ \_ \_ informazioni sul dispositivo HDCP connesso a OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)</span><span class="sxs-lookup"><span data-stu-id="ba838-115">An [**OPM\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ba838-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba838-116">Remarks</span></span>

<span data-ttu-id="ba838-117">Questa query può essere utilizzata solo con la *modalità di emulazione Copp*.</span><span class="sxs-lookup"><span data-stu-id="ba838-117">This query can be used only with *COPP emulation mode*.</span></span> <span data-ttu-id="ba838-118">Se l'interfaccia [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) usa la semantica di output Protection Manager (OPM), questa richiesta di stato non è supportata.</span><span class="sxs-lookup"><span data-stu-id="ba838-118">If the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface uses Output Protection Manager (OPM) semantics, this status request is not supported.</span></span>

<span data-ttu-id="ba838-119">KSV è un identificatore fornito al produttore del dispositivo e viene usato nel processo di autenticazione e configurazione di HDCP.</span><span class="sxs-lookup"><span data-stu-id="ba838-119">The KSV is an identifier provided to the device manufacturer, and is used in the HDCP authentication and setup process.</span></span> <span data-ttu-id="ba838-120">In modalità di emulazione COPP, l'applicazione usa il KSV per determinare se il dispositivo HDCP è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="ba838-120">In COPP emulation mode, the application uses the KSV to determine whether the HDCP device is revoked.</span></span> <span data-ttu-id="ba838-121">In caso contrario, l'applicazione non deve riprodurre contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="ba838-121">If it is, the application should not play protected content.</span></span> <span data-ttu-id="ba838-122">Inoltre, l'applicazione non deve riprodurre contenuto protetto se il dispositivo è un ripetitore HDCP, perché COPP non supporta i ripetitori HDCP.</span><span class="sxs-lookup"><span data-stu-id="ba838-122">Also, the application should not play protected content if the device is an HDCP repeater, because COPP does not support HDCP repeaters.</span></span>

<span data-ttu-id="ba838-123">Questa query non è necessaria quando viene usata la semantica di OPM, perché OPM supporta le revoche di dispositivi e i ripetitori HDCP.</span><span class="sxs-lookup"><span data-stu-id="ba838-123">This query is not needed when OPM semantics are used, because OPM supports device revocation and HDCP repeaters.</span></span>

<span data-ttu-id="ba838-124">Questa query equivale alla \_ query DXVA COPPQueryHDCPKeyData utilizzata in Certified Output Protocol (Copp).</span><span class="sxs-lookup"><span data-stu-id="ba838-124">This query is equivalent to the DXVA\_COPPQueryHDCPKeyData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba838-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba838-125">Requirements</span></span>



| <span data-ttu-id="ba838-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba838-126">Requirement</span></span> | <span data-ttu-id="ba838-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ba838-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ba838-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba838-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ba838-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba838-129">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ba838-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba838-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ba838-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ba838-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ba838-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba838-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba838-133"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba838-133"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba838-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba838-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba838-135">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="ba838-135">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="ba838-136">Richieste di stato di OPM</span><span class="sxs-lookup"><span data-stu-id="ba838-136">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




