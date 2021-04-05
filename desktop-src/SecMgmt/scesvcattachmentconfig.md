---
description: La funzione SceSvcAttachmentConfig viene chiamata dal motore di configurazione della sicurezza quando il sistema è configurato.
ms.assetid: ad20649a-2391-421b-a08c-a4ea6a882abc
title: Funzione di callback SceSvcAttachmentConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentConfig
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c78caa3b8e08ade9c674a11d113a8b91b8f5fad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750871"
---
# <a name="scesvcattachmentconfig-callback-function"></a><span data-ttu-id="e84ad-103">Funzione di callback SceSvcAttachmentConfig</span><span class="sxs-lookup"><span data-stu-id="e84ad-103">SceSvcAttachmentConfig callback function</span></span>

<span data-ttu-id="e84ad-104">La funzione **SceSvcAttachmentConfig** viene chiamata dal motore di configurazione della sicurezza quando il sistema è configurato.</span><span class="sxs-lookup"><span data-stu-id="e84ad-104">The **SceSvcAttachmentConfig** function is called by the Security Configuration Engine when the system is configured.</span></span>

## <a name="syntax"></a><span data-ttu-id="e84ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e84ad-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e84ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e84ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e84ad-107">*pSceCbInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e84ad-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e84ad-108">Puntatore a una struttura di [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) contenente l'handle di database e le funzioni di callback per eseguire query, impostare e liberare informazioni.</span><span class="sxs-lookup"><span data-stu-id="e84ad-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure that contains the database handle and the callback functions to query, set, and free information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e84ad-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e84ad-109">Return value</span></span>

<span data-ttu-id="e84ad-110">Se questa funzione ha esito positivo, restituisce SCESTATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e84ad-110">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="e84ad-111">In caso contrario, restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="e84ad-111">Otherwise it returns an error code.</span></span> <span data-ttu-id="e84ad-112">Per altre informazioni sui codici di errore della configurazione di sicurezza, vedere [valori restituiti degli allegati](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e84ad-112">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e84ad-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e84ad-113">Remarks</span></span>

<span data-ttu-id="e84ad-114">Quando si implementa questa funzione, utilizzare la funzione di callback a cui fa riferimento il membro **pfQueryInfo** della struttura delle [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) per recuperare le informazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="e84ad-114">When implementing this function, use the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve configuration information.</span></span> <span data-ttu-id="e84ad-115">Configurare quindi il servizio usando le informazioni restituite.</span><span class="sxs-lookup"><span data-stu-id="e84ad-115">Then configure the service using the returned information.</span></span>

<span data-ttu-id="e84ad-116">Questa funzione deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e84ad-116">This function must do the following:</span></span>

-   <span data-ttu-id="e84ad-117">Eseguire query sulle informazioni di configurazione dello strumento di configurazione della sicurezza set usando la funzione di callback a cui fa riferimento il membro **pfQueryInfo** della struttura di [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo).</span><span class="sxs-lookup"><span data-stu-id="e84ad-117">Query configuration information from the Security Configuration tool set using the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo).</span></span>
-   <span data-ttu-id="e84ad-118">Configurare il servizio usando le informazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="e84ad-118">Configure the service using the configuration information.</span></span>

<span data-ttu-id="e84ad-119">Per ulteriori informazioni, vedere [implementazione di SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)</span><span class="sxs-lookup"><span data-stu-id="e84ad-119">For more information, see [Implementing SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="e84ad-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e84ad-120">Requirements</span></span>



| <span data-ttu-id="e84ad-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e84ad-121">Requirement</span></span> | <span data-ttu-id="e84ad-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e84ad-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e84ad-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e84ad-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e84ad-124">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e84ad-124">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e84ad-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e84ad-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e84ad-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e84ad-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e84ad-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e84ad-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e84ad-128">**\_informazioni callback \_ SCESVC**</span><span class="sxs-lookup"><span data-stu-id="e84ad-128">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="e84ad-129">**SceSvcAttachmentAnalyze**</span><span class="sxs-lookup"><span data-stu-id="e84ad-129">**SceSvcAttachmentAnalyze**</span></span>](scesvcattachmentanalyze.md)
</dt> </dl>

 

 




