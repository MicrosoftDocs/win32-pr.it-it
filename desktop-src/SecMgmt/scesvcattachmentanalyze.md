---
description: La funzione SceSvcAttachmentAnalyze viene chiamata dal motore di configurazione della sicurezza quando il sistema viene analizzato.
ms.assetid: 8e8a39b9-c4e2-446e-8e0c-eb2113234c1a
title: Funzione di callback SceSvcAttachmentAnalyze
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentAnalyze
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 296d755a0b082b46122432936d30614019b8b9a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750874"
---
# <a name="scesvcattachmentanalyze-callback-function"></a><span data-ttu-id="630e7-103">Funzione di callback SceSvcAttachmentAnalyze</span><span class="sxs-lookup"><span data-stu-id="630e7-103">SceSvcAttachmentAnalyze callback function</span></span>

<span data-ttu-id="630e7-104">La funzione **SceSvcAttachmentAnalyze** viene chiamata dal motore di configurazione della sicurezza quando il sistema viene analizzato.</span><span class="sxs-lookup"><span data-stu-id="630e7-104">The **SceSvcAttachmentAnalyze** function is called by the Security Configuration Engine when the system is analyzed.</span></span>

## <a name="syntax"></a><span data-ttu-id="630e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="630e7-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a><span data-ttu-id="630e7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="630e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="630e7-107">*pSceCbInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="630e7-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="630e7-108">Puntatore a una struttura di [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) che contiene un handle di database opaco e puntatori a funzione di callback per eseguire query, impostare e liberare informazioni.</span><span class="sxs-lookup"><span data-stu-id="630e7-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure which contains an opaque database handle and callback function pointers to query, set, and free information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="630e7-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="630e7-109">Return value</span></span>

<span data-ttu-id="630e7-110">Se questa funzione ha esito positivo, restituisce SCESTATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="630e7-110">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="630e7-111">In caso contrario, restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="630e7-111">Otherwise it returns an error code.</span></span> <span data-ttu-id="630e7-112">Per altre informazioni sui codici di errore della configurazione di sicurezza, vedere [valori restituiti degli allegati](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="630e7-112">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="630e7-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="630e7-113">Remarks</span></span>

<span data-ttu-id="630e7-114">La funzione **SceSvcAttachmentAnalyze** deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="630e7-114">The **SceSvcAttachmentAnalyze** function must do the following:</span></span>

-   <span data-ttu-id="630e7-115">Eseguire query direttamente sulle informazioni di configurazione dal servizio.</span><span class="sxs-lookup"><span data-stu-id="630e7-115">Directly query configuration information from the service.</span></span>
-   <span data-ttu-id="630e7-116">Chiamare la funzione di callback a cui fa riferimento il membro **pfQueryInfo** della struttura delle [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) per recuperare le informazioni dal database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="630e7-116">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve information from the security database.</span></span>
-   <span data-ttu-id="630e7-117">Calcola le differenze tra le informazioni in base al tipo e alla sintassi.</span><span class="sxs-lookup"><span data-stu-id="630e7-117">Compute the differences between the information based on type and syntax.</span></span>
-   <span data-ttu-id="630e7-118">Chiamare la funzione di callback a cui fa riferimento il membro **pfSetInfo** della struttura delle [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) per aggiornare il database di sicurezza con le informazioni del servizio recuperate diverse.</span><span class="sxs-lookup"><span data-stu-id="630e7-118">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo) to update the security database with the retrieved service information that is different.</span></span>

<span data-ttu-id="630e7-119">Per ulteriori informazioni, vedere [implementazione di SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="630e7-119">For more information, see [Implementing SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="630e7-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="630e7-120">Requirements</span></span>



| <span data-ttu-id="630e7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="630e7-121">Requirement</span></span> | <span data-ttu-id="630e7-122">Valore</span><span class="sxs-lookup"><span data-stu-id="630e7-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="630e7-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="630e7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="630e7-124">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="630e7-124">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="630e7-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="630e7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="630e7-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="630e7-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="630e7-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="630e7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="630e7-128">Implementazione di SceSvcAttachmentAnalyze</span><span class="sxs-lookup"><span data-stu-id="630e7-128">Implementing SceSvcAttachmentAnalyze</span></span>](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[<span data-ttu-id="630e7-129">**\_informazioni callback \_ SCESVC**</span><span class="sxs-lookup"><span data-stu-id="630e7-129">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="630e7-130">**SceSvcAttachmentConfig**</span><span class="sxs-lookup"><span data-stu-id="630e7-130">**SceSvcAttachmentConfig**</span></span>](scesvcattachmentconfig.md)
</dt> </dl>

 

 




