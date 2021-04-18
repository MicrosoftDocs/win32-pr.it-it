---
description: La classe provider espone i metodi seguenti.
ms.assetid: AD0BCAC7-6B5C-4BAF-9641-37D315D3E7B1
ms.tgt_platform: multiple
title: Metodi del provider
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb4d8f5d012b5209519670562a7f735a34e6f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318548"
---
# <a name="provider-methods"></a><span data-ttu-id="8f683-103">Metodi del provider</span><span class="sxs-lookup"><span data-stu-id="8f683-103">Provider Methods</span></span>

<span data-ttu-id="8f683-104">\[La classe [**provider**](/windows/desktop/api/Provider/nl-provider-provider) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non saranno disponibili ulteriori attività di sviluppo, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="8f683-104">\[The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="8f683-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="8f683-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="8f683-106">La classe [**provider**](/windows/desktop/api/Provider/nl-provider-provider) espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="8f683-106">The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8f683-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="8f683-107">In this section</span></span>

-   [<span data-ttu-id="8f683-108">**Metodo Commit**</span><span class="sxs-lookup"><span data-stu-id="8f683-108">**Commit method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-commit)
-   [<span data-ttu-id="8f683-109">**Metodo CreateNewInstance**</span><span class="sxs-lookup"><span data-stu-id="8f683-109">**CreateNewInstance method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-createnewinstance)
-   <span data-ttu-id="8f683-110">[**Metodo DeleteInstance**](/windows/desktop/api/Provider/nf-provider-provider-deleteinstance(parsedobjectpath_long_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="8f683-110">[**DeleteInstance method**](/windows/desktop/api/Provider/nf-provider-provider-deleteinstance(parsedobjectpath_long_methodcontext))</span></span>
-   [<span data-ttu-id="8f683-111">**Metodo EnumerateInstances**</span><span class="sxs-lookup"><span data-stu-id="8f683-111">**EnumerateInstances method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-enumerateinstances)
-   <span data-ttu-id="8f683-112">[**Metodo ExecMethod**](/windows/desktop/api/Provider/nf-provider-provider-execmethod(parsedobjectpath_bstr_long_cinstance_cinstance_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="8f683-112">[**ExecMethod method**](/windows/desktop/api/Provider/nf-provider-provider-execmethod(parsedobjectpath_bstr_long_cinstance_cinstance_methodcontext))</span></span>
-   [<span data-ttu-id="8f683-113">**Metodo ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="8f683-113">**ExecQuery method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-execquery)
-   [<span data-ttu-id="8f683-114">**Metodo Flush**</span><span class="sxs-lookup"><span data-stu-id="8f683-114">**Flush method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-flush)
-   [<span data-ttu-id="8f683-115">**Metodo GetLocalComputerName**</span><span class="sxs-lookup"><span data-stu-id="8f683-115">**GetLocalComputerName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getlocalcomputername)
-   [<span data-ttu-id="8f683-116">**Metodo GetLocalInstancePath**</span><span class="sxs-lookup"><span data-stu-id="8f683-116">**GetLocalInstancePath method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getlocalinstancepath)
-   [<span data-ttu-id="8f683-117">**GetNamespace (metodo)**</span><span class="sxs-lookup"><span data-stu-id="8f683-117">**GetNamespace method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getnamespace)
-   <span data-ttu-id="8f683-118">[**Metodo GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))</span><span class="sxs-lookup"><span data-stu-id="8f683-118">[**GetObject method**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))</span></span>
-   [<span data-ttu-id="8f683-119">**GetProviderName (metodo)**</span><span class="sxs-lookup"><span data-stu-id="8f683-119">**GetProviderName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getprovidername)
-   [<span data-ttu-id="8f683-120">**Metodo MakeLocalPath**</span><span class="sxs-lookup"><span data-stu-id="8f683-120">**MakeLocalPath method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-makelocalpath)
-   [<span data-ttu-id="8f683-121">**Metodo del provider**</span><span class="sxs-lookup"><span data-stu-id="8f683-121">**Provider method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-provider)
-   <span data-ttu-id="8f683-122">[**Metodo PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))</span><span class="sxs-lookup"><span data-stu-id="8f683-122">[**PutInstance method**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))</span></span>
-   [<span data-ttu-id="8f683-123">**Metodo SetCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8f683-123">**SetCreationClassName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-setcreationclassname)
-   [<span data-ttu-id="8f683-124">**Metodo ValidateDeletionFlags**</span><span class="sxs-lookup"><span data-stu-id="8f683-124">**ValidateDeletionFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatedeletionflags)
-   [<span data-ttu-id="8f683-125">**Metodo ValidateEnumerationFlags**</span><span class="sxs-lookup"><span data-stu-id="8f683-125">**ValidateEnumerationFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateenumerationflags)
-   [<span data-ttu-id="8f683-126">**Metodo ValidateFlags**</span><span class="sxs-lookup"><span data-stu-id="8f683-126">**ValidateFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateflags)
-   [<span data-ttu-id="8f683-127">**Metodo ValidateGetObjFlags**</span><span class="sxs-lookup"><span data-stu-id="8f683-127">**ValidateGetObjFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validategetobjflags)
-   [<span data-ttu-id="8f683-128">**Metodo ValidateMethodFlags**</span><span class="sxs-lookup"><span data-stu-id="8f683-128">**ValidateMethodFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatemethodflags)
-   [<span data-ttu-id="8f683-129">**Metodo ValidatePutInstanceFlags**</span><span class="sxs-lookup"><span data-stu-id="8f683-129">**ValidatePutInstanceFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateputinstanceflags)
-   [<span data-ttu-id="8f683-130">**Metodo ValidateQueryFlags**</span><span class="sxs-lookup"><span data-stu-id="8f683-130">**ValidateQueryFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatequeryflags)

 

 
