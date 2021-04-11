---
description: 'Il metodo CInstance:: GetWBEMINT64 recupera una proprietà Integer a 64 bit.'
ms.assetid: b51d0c51-3b72-4358-8fc3-d1dbc298b4d9
ms.tgt_platform: multiple
title: 'Metodi CInstance:: GetWBEMINT64 (instance. h)'
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
ms.openlocfilehash: 3d7b7a9f4091125bd722aea197c1670defb0c21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346776"
---
# <a name="cinstancegetwbemint64-methods"></a><span data-ttu-id="9e297-103">Metodi CInstance:: GetWBEMINT64</span><span class="sxs-lookup"><span data-stu-id="9e297-103">CInstance::GetWBEMINT64 methods</span></span>

<span data-ttu-id="9e297-104">\[La classe [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="9e297-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="9e297-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="9e297-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="9e297-106">Il metodo **CInstance:: GetWBEMINT64** recupera una proprietà integer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="9e297-106">The **CInstance::GetWBEMINT64** method retrieves a 64-bit integer property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="9e297-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="9e297-107">Overload list</span></span>



| <span data-ttu-id="9e297-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="9e297-108">Method</span></span>                                                                                   | <span data-ttu-id="9e297-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e297-109">Description</span></span>                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------|
| <span data-ttu-id="9e297-110">[**GetWBEMINT64 (LPCWSTR, LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_longlong_))</span><span class="sxs-lookup"><span data-stu-id="9e297-110">[**GetWBEMINT64(LPCWSTR, LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_longlong_))</span></span>   | <span data-ttu-id="9e297-111">Recupera una proprietà Integer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="9e297-111">Retrieves a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="9e297-112">[**GetWBEMINT64 (LPCWSTR, WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span><span class="sxs-lookup"><span data-stu-id="9e297-112">[**GetWBEMINT64(LPCWSTR, WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span></span> | <span data-ttu-id="9e297-113">Recupera una proprietà Integer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="9e297-113">Retrieves a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="9e297-114">[**GetWBEMINT64 (LPCWSTR, ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span><span class="sxs-lookup"><span data-stu-id="9e297-114">[**GetWBEMINT64(LPCWSTR, ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span></span> | <span data-ttu-id="9e297-115">Recupera una proprietà Integer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="9e297-115">Retrieves a 64-bit integer property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9e297-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e297-116">Requirements</span></span>



| <span data-ttu-id="9e297-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e297-117">Requirement</span></span> | <span data-ttu-id="9e297-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9e297-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e297-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e297-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9e297-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e297-120">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="9e297-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e297-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9e297-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e297-122">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="9e297-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e297-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e297-124"><dt>Istanza. h (includere FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e297-124"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9e297-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="9e297-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e297-126"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e297-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="9e297-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9e297-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e297-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e297-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e297-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e297-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e297-130">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="9e297-130">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

