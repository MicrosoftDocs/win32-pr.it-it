---
description: 'Il metodo CInstance:: GetWBEMINT64 imposta una proprietà Integer a 64 bit.'
audience: developer
ms.assetid: a1789091-ddb6-44f7-bc02-82e7c0209bf9
ms.tgt_platform: multiple
title: 'Metodi CInstance:: SetWBEMINT64 (instance. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f83e39170125a07f28a25d594ad7203f44750a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967978"
---
# <a name="cinstancesetwbemint64-methods"></a><span data-ttu-id="e90fc-103">Metodi CInstance:: SetWBEMINT64</span><span class="sxs-lookup"><span data-stu-id="e90fc-103">CInstance::SetWBEMINT64 methods</span></span>

<span data-ttu-id="e90fc-104">\[La classe [**CInstance**](/windows/win32/api/instance/nl-instance-cinstance) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="e90fc-104">\[The [**CInstance**](/windows/win32/api/instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="e90fc-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="e90fc-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="e90fc-106">Il metodo [**CInstance:: GetWBEMINT64**](cinstance-getwbemint64.md) imposta una proprietà integer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="e90fc-106">The [**CInstance::GetWBEMINT64**](cinstance-getwbemint64.md) method sets a 64-bit integer property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="e90fc-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="e90fc-107">Overload list</span></span>



| <span data-ttu-id="e90fc-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="e90fc-108">Method</span></span>                                                                                               | <span data-ttu-id="e90fc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e90fc-109">Description</span></span>                                |
|:-----------------------------------------------------------------------------------------------------|:-------------------------------------------|
| <span data-ttu-id="e90fc-110">[**SetWBEMINT64 (LPCWSTR, const LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constlonglong))</span><span class="sxs-lookup"><span data-stu-id="e90fc-110">[**SetWBEMINT64(LPCWSTR, const LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constlonglong))</span></span>    | <span data-ttu-id="e90fc-111">Imposta una proprietà Integer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="e90fc-111">Sets a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="e90fc-112">[**SetWBEMINT64 (LPCWSTR, const WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span><span class="sxs-lookup"><span data-stu-id="e90fc-112">[**SetWBEMINT64(LPCWSTR, const WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span></span> | <span data-ttu-id="e90fc-113">Imposta una proprietà Integer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="e90fc-113">Sets a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="e90fc-114">[**SetWBEMINT64 (LPCWSTR, const ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span><span class="sxs-lookup"><span data-stu-id="e90fc-114">[**SetWBEMINT64(LPCWSTR, const ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span></span>  | <span data-ttu-id="e90fc-115">Imposta una proprietà Integer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="e90fc-115">Sets a 64-bit integer property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e90fc-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e90fc-116">Requirements</span></span>



| <span data-ttu-id="e90fc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e90fc-117">Requirement</span></span> | <span data-ttu-id="e90fc-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e90fc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e90fc-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e90fc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e90fc-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e90fc-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="e90fc-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e90fc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e90fc-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e90fc-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="e90fc-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e90fc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e90fc-124"><dt>Istanza. h (includere FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e90fc-124"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e90fc-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="e90fc-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="e90fc-126"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e90fc-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="e90fc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e90fc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e90fc-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e90fc-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e90fc-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e90fc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e90fc-130">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="e90fc-130">**CInstance**</span></span>](/windows/win32/api/instance/nl-instance-cinstance)
</dt> </dl>

<span data-ttu-id="e90fc-131">�</span><span class="sxs-lookup"><span data-stu-id="e90fc-131">�</span></span>

<span data-ttu-id="e90fc-132">�</span><span class="sxs-lookup"><span data-stu-id="e90fc-132">�</span></span>
