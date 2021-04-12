---
title: Funzioni di callback dell'applicazione client
description: Due tipi di firme di callback.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371edd162c4cbd1332764c7b3e9e70bf114270e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396586"
---
# <a name="client-application-callback-functions"></a><span data-ttu-id="ac3b6-103">Funzioni di callback dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="ac3b6-103">Client Application Callback Functions</span></span>

<span data-ttu-id="ac3b6-104">Il Windows Biometric Framework supporta due tipi di firme di callback.</span><span class="sxs-lookup"><span data-stu-id="ac3b6-104">The Windows Biometric Framework supports two types of callback signatures.</span></span> <span data-ttu-id="ac3b6-105">A partire da Windows 8, il callback seguente è supportato.</span><span class="sxs-lookup"><span data-stu-id="ac3b6-105">Beginning with Windows 8, the following callback is supported.</span></span> <span data-ttu-id="ac3b6-106">Si consiglia di implementare questo callback per tutte le nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ac3b6-106">We recommend that you implement this callback for all new applications.</span></span> <span data-ttu-id="ac3b6-107">Questo callback, tuttavia, non può essere usato in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ac3b6-107">This callback cannot, however, be used in Windows 7.</span></span>



| <span data-ttu-id="ac3b6-108">Callback</span><span class="sxs-lookup"><span data-stu-id="ac3b6-108">Callback</span></span>                                                                                     | <span data-ttu-id="ac3b6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac3b6-109">Description</span></span>                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac3b6-110">**\_callback di \_ completamento \_ asincrono PWINBIO**</span><span class="sxs-lookup"><span data-stu-id="ac3b6-110">**PWINBIO\_ASYNC\_COMPLETION\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | <span data-ttu-id="ac3b6-111">Notifica all'applicazione client che un'operazione asincrona avviata tramite [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) o [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ac3b6-111">Notifies the client application that an asynchronous operation started by using [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) or [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) has completed.</span></span><br/> |



 

<span data-ttu-id="ac3b6-112">Le funzioni di callback seguenti sono state introdotte in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ac3b6-112">The following callback functions were introduced in Windows 7.</span></span> <span data-ttu-id="ac3b6-113">Si consiglia di non implementarli per le nuove applicazioni destinate a sistemi operativi Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ac3b6-113">We recommend that you do not implement them for new applications that target Windows 8 and later operating systems.</span></span>



| <span data-ttu-id="ac3b6-114">Callback</span><span class="sxs-lookup"><span data-stu-id="ac3b6-114">Callback</span></span>                                                                                 | <span data-ttu-id="ac3b6-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac3b6-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac3b6-116">**\_callback di acquisizione PWINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="ac3b6-116">**PWINBIO\_CAPTURE\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | <span data-ttu-id="ac3b6-117">Restituisce i risultati della funzione asincrona [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) .</span><span class="sxs-lookup"><span data-stu-id="ac3b6-117">Returns results from the asynchronous [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) function.</span></span><br/> |
| [<span data-ttu-id="ac3b6-118">**\_callback di \_ acquisizione \_ registrazione PWINBIO**</span><span class="sxs-lookup"><span data-stu-id="ac3b6-118">**PWINBIO\_ENROLL\_CAPTURE\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | <span data-ttu-id="ac3b6-119">Restituisce i risultati della funzione asincrona [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) .</span><span class="sxs-lookup"><span data-stu-id="ac3b6-119">Returns results from the asynchronous [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) function.</span></span><br/> |
| [<span data-ttu-id="ac3b6-120">**\_callback evento \_ PWINBIO**</span><span class="sxs-lookup"><span data-stu-id="ac3b6-120">**PWINBIO\_EVENT\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | <span data-ttu-id="ac3b6-121">Restituisce i risultati della funzione asincrona [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) .</span><span class="sxs-lookup"><span data-stu-id="ac3b6-121">Returns results from the asynchronous [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function.</span></span><br/>           |
| [<span data-ttu-id="ac3b6-122">**\_callback di identificazione PWINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="ac3b6-122">**PWINBIO\_IDENTIFY\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | <span data-ttu-id="ac3b6-123">Restituisce i risultati della funzione asincrona [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) .</span><span class="sxs-lookup"><span data-stu-id="ac3b6-123">Returns results from the asynchronous [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) function.</span></span><br/>           |
| [<span data-ttu-id="ac3b6-124">**PWINBIO \_ individuare \_ il \_ callback del sensore**</span><span class="sxs-lookup"><span data-stu-id="ac3b6-124">**PWINBIO\_LOCATE\_SENSOR\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | <span data-ttu-id="ac3b6-125">Restituisce i risultati della funzione asincrona [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) .</span><span class="sxs-lookup"><span data-stu-id="ac3b6-125">Returns results from the asynchronous [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) function.</span></span><br/>   |
| [<span data-ttu-id="ac3b6-126">**PWINBIO \_ verifica \_ callback**</span><span class="sxs-lookup"><span data-stu-id="ac3b6-126">**PWINBIO\_VERIFY\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | <span data-ttu-id="ac3b6-127">Restituisce i risultati della funzione asincrona [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) .</span><span class="sxs-lookup"><span data-stu-id="ac3b6-127">Returns results from the asynchronous [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) function.</span></span><br/>               |



 

## <a name="related-topics"></a><span data-ttu-id="ac3b6-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ac3b6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac3b6-129">Riferimento all'applicazione client</span><span class="sxs-lookup"><span data-stu-id="ac3b6-129">Client Application Reference</span></span>](client-application-reference.md)
</dt> </dl>

 

 





