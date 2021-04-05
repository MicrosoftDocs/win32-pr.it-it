---
description: La funzione SceSvcAttachmentUpdate viene chiamata dagli snap-in di configurazione di sicurezza per passare le modifiche di configurazione al database di sicurezza.
ms.assetid: 2b5b3718-8ccb-480a-97fb-c8115d8f3a5c
title: Funzione di callback SceSvcAttachmentUpdate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentUpdate
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5bc4c9426f6a085c72f2fc3d872de4d7da59156b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750866"
---
# <a name="scesvcattachmentupdate-callback-function"></a><span data-ttu-id="0745a-103">Funzione di callback SceSvcAttachmentUpdate</span><span class="sxs-lookup"><span data-stu-id="0745a-103">SceSvcAttachmentUpdate callback function</span></span>

<span data-ttu-id="0745a-104">La funzione **SceSvcAttachmentUpdate** viene chiamata dagli snap-in di configurazione di sicurezza per passare le modifiche di configurazione al database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0745a-104">The **SceSvcAttachmentUpdate** function is called by the Security Configuration snap-ins to pass configuration changes to the security database.</span></span>

## <a name="syntax"></a><span data-ttu-id="0745a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0745a-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate(
  _In_ PSCESVC_CALLBACK_INFO     pSceCbInfo,
  _In_ SCESVC_CONFIGURATION_INFO *ServiceInfo
);
```



## <a name="parameters"></a><span data-ttu-id="0745a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0745a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0745a-107">*pSceCbInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0745a-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0745a-108">Puntatore a una struttura di [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) contenente l'handle di callback e i puntatori a funzione per SCE.</span><span class="sxs-lookup"><span data-stu-id="0745a-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure which contains the callback handle and function pointers to SCE.</span></span>

</dd> <dt>

<span data-ttu-id="0745a-109">*ServiceInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0745a-109">*ServiceInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0745a-110">Informazioni di configurazione aggiornate.</span><span class="sxs-lookup"><span data-stu-id="0745a-110">Updated configuration information.</span></span> <span data-ttu-id="0745a-111">La struttura di dati usata per queste informazioni è [**SCESVC \_ Configuration \_ info**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).</span><span class="sxs-lookup"><span data-stu-id="0745a-111">The data structure used for this information is [**SCESVC\_CONFIGURATION\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0745a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0745a-112">Return value</span></span>

<span data-ttu-id="0745a-113">Se questa funzione ha esito positivo, restituisce SCESTATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0745a-113">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="0745a-114">In caso contrario, restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="0745a-114">Otherwise it returns an error code.</span></span> <span data-ttu-id="0745a-115">Per altre informazioni sui codici di errore della configurazione di sicurezza, vedere [valori restituiti degli allegati](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0745a-115">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0745a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0745a-116">Remarks</span></span>

<span data-ttu-id="0745a-117">La funzione **SceSvcAttachmentUpdate** deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0745a-117">The **SceSvcAttachmentUpdate** function must do the following:</span></span>

-   <span data-ttu-id="0745a-118">Chiamare la funzione di callback a cui fa riferimento il membro **pfQueryInfo** della struttura delle [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) per recuperare le informazioni di configurazione di base correnti dal database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0745a-118">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve the current base configuration information from the security database.</span></span>
-   <span data-ttu-id="0745a-119">Chiamare la funzione di callback a cui fa riferimento il membro **pfQueryInfo** della struttura delle [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) per recuperare l'ultimo set di differenze (informazioni di analisi) dal database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0745a-119">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve the last set of differences (analysis information) from the security database.</span></span>
-   <span data-ttu-id="0745a-120">Usare le informazioni sul servizio fornite (vedere *ServiceInfo*) per calcolare la nuova configurazione di base.</span><span class="sxs-lookup"><span data-stu-id="0745a-120">Use the supplied service information (see *ServiceInfo*) to compute the new base configuration.</span></span>
-   <span data-ttu-id="0745a-121">Usare le informazioni sul servizio fornite (vedere *ServiceInfo*) e l'analisi per calcolare le nuove informazioni sulle differenze.</span><span class="sxs-lookup"><span data-stu-id="0745a-121">Use the supplied service information (see *ServiceInfo*) and the analysis to compute the new difference information.</span></span>
-   <span data-ttu-id="0745a-122">Chiamare la funzione di callback a cui fa riferimento il membro **pfSetInfo** della struttura delle [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) per impostare la nuova configurazione di base nel database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0745a-122">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo)to set the new base configuration in the security database.</span></span>
-   <span data-ttu-id="0745a-123">Chiamare la funzione di callback a cui fa riferimento il membro **pfSetInfo** della struttura delle [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) per impostare le nuove informazioni di analisi nel database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0745a-123">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo) to set the new analysis information in the security database.</span></span>

<span data-ttu-id="0745a-124">Per ulteriori informazioni, vedere [implementazione di SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)</span><span class="sxs-lookup"><span data-stu-id="0745a-124">For more information, see [Implementing SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="0745a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0745a-125">Requirements</span></span>



| <span data-ttu-id="0745a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0745a-126">Requirement</span></span> | <span data-ttu-id="0745a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="0745a-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0745a-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0745a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0745a-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0745a-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0745a-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0745a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0745a-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0745a-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0745a-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0745a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0745a-133">**\_informazioni callback \_ SCESVC**</span><span class="sxs-lookup"><span data-stu-id="0745a-133">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="0745a-134">**\_informazioni di configurazione di SCESVC \_**</span><span class="sxs-lookup"><span data-stu-id="0745a-134">**SCESVC\_CONFIGURATION\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info)
</dt> </dl>

 

 




