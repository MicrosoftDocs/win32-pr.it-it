---
description: Specifica se a un'applicazione è consentito l'accesso ai frame video non compressi.
ms.assetid: 7D2A9003-B36E-4082-877E-8AC7F5645E89
title: Attributo MFPROTECTION_VIDEO_FRAMES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8ccfc56fb1c1b52b14e16d8e702111f3d8564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310248"
---
# <a name="mfprotection_video_frames-attribute"></a><span data-ttu-id="de03f-103">MFPROTECTION \_ \_ attributo video frames</span><span class="sxs-lookup"><span data-stu-id="de03f-103">MFPROTECTION\_VIDEO\_FRAMES attribute</span></span>

<span data-ttu-id="de03f-104">Specifica se a un'applicazione è consentito l'accesso ai frame video non compressi.</span><span class="sxs-lookup"><span data-stu-id="de03f-104">Specifies if an application is allowed access to uncompressed video frames.</span></span>

## <a name="data-type"></a><span data-ttu-id="de03f-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="de03f-105">Data type</span></span>

<span data-ttu-id="de03f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="de03f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="de03f-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="de03f-107">Remarks</span></span>

<span data-ttu-id="de03f-108">Il valore 0 indica che l'applicazione è autorizzata ad accedere ai frame.</span><span class="sxs-lookup"><span data-stu-id="de03f-108">A value of 0 indicates that the application is allowed access to the frames.</span></span> <span data-ttu-id="de03f-109">Questo potrebbe essere determinato in seguito a un contratto privato tra l'applicazione e il particolare sistema di protezione del contenuto in uso.</span><span class="sxs-lookup"><span data-stu-id="de03f-109">This might be determined as a result of a private agreement between the application and the particular content protection system in use.</span></span>

<span data-ttu-id="de03f-110">Il valore 1 indica che l'applicazione è autorizzata ad accedere ai frame se l'applicazione fornisce un certificato dell'applicazione valido (vedere [**IMFMediaEngineProtectedContent:: SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).</span><span class="sxs-lookup"><span data-stu-id="de03f-110">A value of 1 indicates that the application is allowed access to frames if a valid application certificate is provided by the application (see [**IMFMediaEngineProtectedContent::SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).</span></span>

<span data-ttu-id="de03f-111">Il valore 0xFFFFFFFF, che corrisponde al valore predefinito, indica che non è consentito l'accesso alle applicazioni ai frame non compressi.</span><span class="sxs-lookup"><span data-stu-id="de03f-111">A value of 0xFFFFFFFF, which is the default value, indicates no applications are allowed access to uncompressed frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="de03f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de03f-112">Requirements</span></span>



| <span data-ttu-id="de03f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="de03f-113">Requirement</span></span> | <span data-ttu-id="de03f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="de03f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="de03f-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de03f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="de03f-116">\[Solo app UWP Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="de03f-116">Windows 8 \[UWP apps only\]</span></span><br/>                                             |
| <span data-ttu-id="de03f-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de03f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="de03f-118">\[Solo app UWP Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="de03f-118">Windows Server 2012 \[UWP apps only\]</span></span><br/>                                   |
| <span data-ttu-id="de03f-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de03f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="de03f-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="de03f-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de03f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de03f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de03f-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="de03f-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="de03f-123">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="de03f-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




