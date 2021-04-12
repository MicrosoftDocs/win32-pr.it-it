---
description: Metodo di overload che rilascia la memoria che contiene il percorso.
audience: developer
ms.assetid: 9164d7b2-15b8-4b73-ab8c-68ed45692ea0
ms.tgt_platform: multiple
title: 'Metodi CObjectPathParser:: Free (ObjPath. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 86494e569f68d8eff8b691c648ec5e221b28b39d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232636"
---
# <a name="cobjectpathparserfree-methods"></a><span data-ttu-id="da2e7-103">Metodi CObjectPathParser:: Free</span><span class="sxs-lookup"><span data-stu-id="da2e7-103">CObjectPathParser::Free methods</span></span>

<span data-ttu-id="da2e7-104">\[La classe [**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="da2e7-104">\[The [**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="da2e7-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="da2e7-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="da2e7-106">Metodo di overload che rilascia la memoria che contiene il percorso.</span><span class="sxs-lookup"><span data-stu-id="da2e7-106">An overloaded method that releases the memory that contains the path.</span></span>

### <a name="overload-list"></a><span data-ttu-id="da2e7-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="da2e7-107">Overload list</span></span>



| <span data-ttu-id="da2e7-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="da2e7-108">Method</span></span>                                                                     | <span data-ttu-id="da2e7-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da2e7-109">Description</span></span>                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| <span data-ttu-id="da2e7-110">[**Gratuito (LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))</span><span class="sxs-lookup"><span data-stu-id="da2e7-110">[**Free(LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))</span></span>                     | <span data-ttu-id="da2e7-111">Rilascia la memoria che contiene il percorso non analizzato.</span><span class="sxs-lookup"><span data-stu-id="da2e7-111">Releases the memory that contains the unparsed path.</span></span><br/>                      |
| <span data-ttu-id="da2e7-112">[**Gratuito (ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath))</span><span class="sxs-lookup"><span data-stu-id="da2e7-112">[**Free(ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath))</span></span> | <span data-ttu-id="da2e7-113">Rilascia la memoria che contiene la struttura con il percorso analizzato.</span><span class="sxs-lookup"><span data-stu-id="da2e7-113">Releases the memory that contains the structure that has the parsed path.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="da2e7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da2e7-114">Requirements</span></span>



| <span data-ttu-id="da2e7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="da2e7-115">Requirement</span></span> | <span data-ttu-id="da2e7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="da2e7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da2e7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da2e7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="da2e7-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da2e7-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="da2e7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da2e7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="da2e7-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da2e7-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="da2e7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da2e7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="da2e7-122"><dt>ObjPath. h (include ObjPath. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da2e7-122"><dt>ObjPath.h (include ObjPath.h)</dt></span></span> </dl>                                                      |
| <span data-ttu-id="da2e7-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="da2e7-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="da2e7-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da2e7-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="da2e7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="da2e7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da2e7-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da2e7-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da2e7-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da2e7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da2e7-128">**CObjectPathParser**</span><span class="sxs-lookup"><span data-stu-id="da2e7-128">**CObjectPathParser**</span></span>](/windows/win32/api/objpath/nl-objpath-cobjectpathparser)
</dt> </dl>

<span data-ttu-id="da2e7-129">�</span><span class="sxs-lookup"><span data-stu-id="da2e7-129">�</span></span>

<span data-ttu-id="da2e7-130">�</span><span class="sxs-lookup"><span data-stu-id="da2e7-130">�</span></span>
