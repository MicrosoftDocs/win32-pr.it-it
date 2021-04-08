---
description: La classe CWbemProviderGlue espone i metodi seguenti.
ms.assetid: E09290AF-1C2E-458A-811E-5357D470D3DF
ms.tgt_platform: multiple
title: Metodi CWbemProviderGlue
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea54ffdeaa6b74cda3b830ea65fdc17f8ffa129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967661"
---
# <a name="cwbemproviderglue-methods"></a><span data-ttu-id="72919-103">Metodi CWbemProviderGlue</span><span class="sxs-lookup"><span data-stu-id="72919-103">CWbemProviderGlue Methods</span></span>

<span data-ttu-id="72919-104">\[La classe [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="72919-104">\[The [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="72919-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="72919-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="72919-106">La classe [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="72919-106">The [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="72919-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="72919-107">In this section</span></span>

-   <span data-ttu-id="72919-108">[**Metodo FrameworkLoginDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong))</span><span class="sxs-lookup"><span data-stu-id="72919-108">[**FrameworkLoginDLL method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong))</span></span>
-   <span data-ttu-id="72919-109">[**Metodo FrameworkLogoffDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong))</span><span class="sxs-lookup"><span data-stu-id="72919-109">[**FrameworkLogoffDLL method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong))</span></span>
-   <span data-ttu-id="72919-110">[**Metodo GetAllDerivedInstances**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallderivedinstances(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="72919-110">[**GetAllDerivedInstances method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallderivedinstances(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span></span>
-   [<span data-ttu-id="72919-111">**Metodo GetAllDerivedInstancesAsynch**</span><span class="sxs-lookup"><span data-stu-id="72919-111">**GetAllDerivedInstancesAsynch method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallderivedinstancesasynch)
-   [<span data-ttu-id="72919-112">**Metodo GetAllInstances**</span><span class="sxs-lookup"><span data-stu-id="72919-112">**GetAllInstances method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallinstances)
-   [<span data-ttu-id="72919-113">**Metodo GetAllInstancesAsynch**</span><span class="sxs-lookup"><span data-stu-id="72919-113">**GetAllInstancesAsynch method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallinstancesasynch)
-   <span data-ttu-id="72919-114">[**Metodi GetEmptyInstance**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="72919-114">[**GetEmptyInstance methods**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span>
-   <span data-ttu-id="72919-115">[**Metodo GetInstanceByPath**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancebypath(lpcwstr_cinstance_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="72919-115">[**GetInstanceByPath method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancebypath(lpcwstr_cinstance_methodcontext))</span></span>
-   [<span data-ttu-id="72919-116">**Metodo GetInstanceKeysByPath**</span><span class="sxs-lookup"><span data-stu-id="72919-116">**GetInstanceKeysByPath method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancekeysbypath)
-   [<span data-ttu-id="72919-117">**Metodo GetInstancePropertiesByPath**</span><span class="sxs-lookup"><span data-stu-id="72919-117">**GetInstancePropertiesByPath method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancepropertiesbypath)
-   <span data-ttu-id="72919-118">[**Metodo GetInstancesByQuery**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancesbyquery(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="72919-118">[**GetInstancesByQuery method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancesbyquery(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span></span>
-   [<span data-ttu-id="72919-119">**Metodo GetInstancesByQueryAsynch**</span><span class="sxs-lookup"><span data-stu-id="72919-119">**GetInstancesByQueryAsynch method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancesbyqueryasynch)
-   <span data-ttu-id="72919-120">[**Metodo GetNameSpaceConnection**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getnamespaceconnection(lpcwstr_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="72919-120">[**GetNameSpaceConnection method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getnamespaceconnection(lpcwstr_methodcontext))</span></span>
-   <span data-ttu-id="72919-121">[**Metodo IsDerivedFrom**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-isderivedfrom(lpcwstr_lpcwstr_methodcontext_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="72919-121">[**IsDerivedFrom method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-isderivedfrom(lpcwstr_lpcwstr_methodcontext_lpcwstr))</span></span>
-   [<span data-ttu-id="72919-122">**Metodo SetStatusObject**</span><span class="sxs-lookup"><span data-stu-id="72919-122">**SetStatusObject method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-setstatusobject)

 

 
