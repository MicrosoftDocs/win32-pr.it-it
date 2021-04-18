---
description: 'Il metodo CInstance:: SetCHString imposta una proprietà di stringa.'
ms.assetid: a75b574d-9ee7-4930-a003-5d71c5f1d687
ms.tgt_platform: multiple
title: 'Metodi CInstance:: SetCHString (instance. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 187c07b5cf0f867ee838f2f3725d6a82319d4634
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315245"
---
# <a name="cinstancesetchstring-methods"></a><span data-ttu-id="165b6-103">Metodi CInstance:: SetCHString</span><span class="sxs-lookup"><span data-stu-id="165b6-103">CInstance::SetCHString methods</span></span>

<span data-ttu-id="165b6-104">\[La classe [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="165b6-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="165b6-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="165b6-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="165b6-106">Il metodo **CInstance:: SetCHString** imposta una proprietà di stringa.</span><span class="sxs-lookup"><span data-stu-id="165b6-106">The **CInstance::SetCHString** method sets a string property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="165b6-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="165b6-107">Overload list</span></span>



| <span data-ttu-id="165b6-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="165b6-108">Method</span></span>                                                                                           | <span data-ttu-id="165b6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="165b6-109">Description</span></span>                        |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span data-ttu-id="165b6-110">[**SetCHString (LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setchstring(lpcwstr_lpcstr))</span><span class="sxs-lookup"><span data-stu-id="165b6-110">[**SetCHString(LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setchstring(lpcwstr_lpcstr))</span></span>                   | <span data-ttu-id="165b6-111">Imposta una proprietà di stringa.</span><span class="sxs-lookup"><span data-stu-id="165b6-111">Sets a string property.</span></span><br/> |
| <span data-ttu-id="165b6-112">[**SetCHString (LPCWSTR, const CHString&)**](/windows/win32/api/instance/nf-instance-cinstance-setchstring(lpcwstr_constchstring_))</span><span class="sxs-lookup"><span data-stu-id="165b6-112">[**SetCHString(LPCWSTR, const CHString&)**](/windows/win32/api/instance/nf-instance-cinstance-setchstring(lpcwstr_constchstring_))</span></span> | <span data-ttu-id="165b6-113">Imposta una proprietà di stringa.</span><span class="sxs-lookup"><span data-stu-id="165b6-113">Sets a string property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="165b6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="165b6-114">Requirements</span></span>



| <span data-ttu-id="165b6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="165b6-115">Requirement</span></span> | <span data-ttu-id="165b6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="165b6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="165b6-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="165b6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="165b6-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="165b6-118">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="165b6-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="165b6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="165b6-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="165b6-120">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="165b6-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="165b6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="165b6-122"><dt>Istanza. h (includere FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="165b6-122"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="165b6-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="165b6-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="165b6-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="165b6-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="165b6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="165b6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="165b6-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="165b6-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="165b6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="165b6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="165b6-128">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="165b6-128">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

