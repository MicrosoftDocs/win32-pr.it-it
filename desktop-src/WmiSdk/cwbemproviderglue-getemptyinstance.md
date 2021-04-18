---
description: Il metodo GetEmptyInstance recupera una singola istanza non popolata della classe specificata.
audience: developer
ms.assetid: 2873b466-3782-4d63-a777-5b25e3fb7615
ms.tgt_platform: multiple
title: 'Metodi CWbemProviderGlue:: GetEmptyInstance (WbemGlue. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 853afbf3789969fbfca66d5f9cb40f41eadf7630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310384"
---
# <a name="cwbemprovidergluegetemptyinstance-methods"></a><span data-ttu-id="451ed-103">Metodi CWbemProviderGlue:: GetEmptyInstance</span><span class="sxs-lookup"><span data-stu-id="451ed-103">CWbemProviderGlue::GetEmptyInstance methods</span></span>

<span data-ttu-id="451ed-104">\[La classe [**CWbemProviderGlue**](/windows/win32/api/wbemglue/nl-wbemglue-cwbemproviderglue) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="451ed-104">\[The [**CWbemProviderGlue**](/windows/win32/api/wbemglue/nl-wbemglue-cwbemproviderglue) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="451ed-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="451ed-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="451ed-106">Il metodo **GetEmptyInstance** recupera una singola istanza non popolata della classe specificata.</span><span class="sxs-lookup"><span data-stu-id="451ed-106">The **GetEmptyInstance** method retrieves a single unpopulated instance of the specified class.</span></span>

### <a name="overload-list"></a><span data-ttu-id="451ed-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="451ed-107">Overload list</span></span>



| <span data-ttu-id="451ed-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="451ed-108">Method</span></span>                                                                                                                                            | <span data-ttu-id="451ed-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="451ed-109">Description</span></span>                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| <span data-ttu-id="451ed-110">[**GetEmptyInstance (LPCWSTR, CInstance, LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="451ed-110">[**GetEmptyInstance(LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span>                            | <span data-ttu-id="451ed-111">Recupera una singola istanza non popolata della classe specificata.</span><span class="sxs-lookup"><span data-stu-id="451ed-111">Retrieves a single unpopulated instance of the specified class.</span></span><br/> |
| <span data-ttu-id="451ed-112">[**GetEmptyInstance (MethodContext, LPCWSTR, CInstance, LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="451ed-112">[**GetEmptyInstance(MethodContext,LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span> | <span data-ttu-id="451ed-113">Recupera una singola istanza non popolata della classe specificata.</span><span class="sxs-lookup"><span data-stu-id="451ed-113">Retrieves a single unpopulated instance of the specified class.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="451ed-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="451ed-114">Requirements</span></span>



| <span data-ttu-id="451ed-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="451ed-115">Requirement</span></span> | <span data-ttu-id="451ed-116">Valore</span><span class="sxs-lookup"><span data-stu-id="451ed-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="451ed-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="451ed-117">Minimum supported client</span></span><br/> | <span data-ttu-id="451ed-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="451ed-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="451ed-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="451ed-119">Minimum supported server</span></span><br/> | <span data-ttu-id="451ed-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="451ed-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="451ed-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="451ed-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="451ed-122"><dt>WbemGlue. h (include FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="451ed-122"><dt>WbemGlue.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="451ed-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="451ed-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="451ed-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="451ed-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="451ed-125">DLL</span><span class="sxs-lookup"><span data-stu-id="451ed-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="451ed-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="451ed-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="451ed-127">�</span><span class="sxs-lookup"><span data-stu-id="451ed-127">�</span></span>

<span data-ttu-id="451ed-128">�</span><span class="sxs-lookup"><span data-stu-id="451ed-128">�</span></span>
