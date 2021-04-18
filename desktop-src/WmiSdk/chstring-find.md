---
description: Il metodo Find Cerca in una stringa la prima corrispondenza di una sottostringa.
audience: developer
ms.assetid: 98a7c5ad-5bc7-4918-b978-45d2b439f250
ms.tgt_platform: multiple
title: 'Metodi CHString:: Find (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5996ca5c06e2101fad834ce2e37df31ee435fbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319309"
---
# <a name="chstringfind-methods"></a><span data-ttu-id="c3968-103">Metodi CHString:: Find</span><span class="sxs-lookup"><span data-stu-id="c3968-103">CHString::Find methods</span></span>

<span data-ttu-id="c3968-104">\[La classe [**CHString**](chstring.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="c3968-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="c3968-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="c3968-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="c3968-106">Il metodo **Find** Cerca in una stringa la prima corrispondenza di una sottostringa.</span><span class="sxs-lookup"><span data-stu-id="c3968-106">The **Find** method searches a string for the first match of a substring.</span></span>

### <a name="overload-list"></a><span data-ttu-id="c3968-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="c3968-107">Overload list</span></span>



| <span data-ttu-id="c3968-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="c3968-108">Method</span></span>                                          | <span data-ttu-id="c3968-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3968-109">Description</span></span>                                             |
|:------------------------------------------------|:--------------------------------------------------------|
| <span data-ttu-id="c3968-110">[**Trova (WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="c3968-110">[**Find(WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span></span>     | <span data-ttu-id="c3968-111">Cerca il **WSTR** in questa stringa.</span><span class="sxs-lookup"><span data-stu-id="c3968-111">Searches for the **WSTR** in this string.</span></span><br/>    |
| <span data-ttu-id="c3968-112">[**Trova (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="c3968-112">[**Find(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span></span> | <span data-ttu-id="c3968-113">Cerca il **LPCWSTR** in questa stringa.</span><span class="sxs-lookup"><span data-stu-id="c3968-113">Searches for the **LPCWSTR** in this string.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c3968-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3968-114">Requirements</span></span>



| <span data-ttu-id="c3968-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3968-115">Requirement</span></span> | <span data-ttu-id="c3968-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c3968-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3968-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3968-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c3968-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3968-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="c3968-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3968-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c3968-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3968-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="c3968-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c3968-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3968-122"><dt>ChString. h (include FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3968-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c3968-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="c3968-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c3968-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3968-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="c3968-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c3968-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3968-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3968-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="c3968-127">�</span><span class="sxs-lookup"><span data-stu-id="c3968-127">�</span></span>

<span data-ttu-id="c3968-128">�</span><span class="sxs-lookup"><span data-stu-id="c3968-128">�</span></span>
