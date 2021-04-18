---
description: Il costruttore della classe WBEMTime facilita le conversioni tra diversi formati di runtime di Windows e ANSI C.
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: 'Costruttori WBEMTime:: WBEMTime (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 778b9af2e732b3d294b0348ff2d2b91b60518d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318848"
---
# <a name="wbemtimewbemtime-constructors"></a><span data-ttu-id="5a1f8-103">Costruttori WBEMTime:: WBEMTime</span><span class="sxs-lookup"><span data-stu-id="5a1f8-103">WBEMTime::WBEMTime constructors</span></span>

<span data-ttu-id="5a1f8-104">\[La classe [**WBEMTime**](wbemtime.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="5a1f8-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="5a1f8-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="5a1f8-106">Il costruttore della classe **WBEMTime** facilita le conversioni tra diversi formati di runtime di Windows e ANSI C.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-106">The **WBEMTime** class constructor facilitates conversions between various Windows and ANSI C run-time time formats.</span></span>

### <a name="overload-list"></a><span data-ttu-id="5a1f8-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="5a1f8-107">Overload list</span></span>



| <span data-ttu-id="5a1f8-108">Costruttore</span><span class="sxs-lookup"><span data-stu-id="5a1f8-108">Constructor</span></span>                                                                 | <span data-ttu-id="5a1f8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a1f8-109">Description</span></span>                                                               |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span data-ttu-id="5a1f8-110">[**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="5a1f8-110">[**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>                                   | <span data-ttu-id="5a1f8-111">Crea un oggetto ora non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-111">Creates an uninitialized time object.</span></span><br/>                          |
| <span data-ttu-id="5a1f8-112">[**WBEMTime (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="5a1f8-112">[**WBEMTime(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>                           | <span data-ttu-id="5a1f8-113">Inizializza il nuovo oggetto Time sul valore nel parametro.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-113">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="5a1f8-114">[**WBEMTime (const time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="5a1f8-114">[**WBEMTime(const time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))</span></span>        | <span data-ttu-id="5a1f8-115">Inizializza il nuovo oggetto Time sul valore nel parametro.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-115">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="5a1f8-116">[**WBEMTime (const struct TM)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))</span><span class="sxs-lookup"><span data-stu-id="5a1f8-116">[**WBEMTime(const struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))</span></span>    | <span data-ttu-id="5a1f8-117">Inizializza il nuovo oggetto Time sul valore nel parametro.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-117">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="5a1f8-118">[**WBEMTime (const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="5a1f8-118">[**WBEMTime(const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))</span></span>     | <span data-ttu-id="5a1f8-119">Inizializza il nuovo oggetto Time sul valore nel parametro.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-119">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="5a1f8-120">[**WBEMTime (const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_))</span><span class="sxs-lookup"><span data-stu-id="5a1f8-120">[**WBEMTime(const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_))</span></span> | <span data-ttu-id="5a1f8-121">Inizializza il nuovo oggetto Time sul valore nel parametro.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-121">Initializes the new time object to the value in the parameter.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5a1f8-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a1f8-122">Requirements</span></span>



| <span data-ttu-id="5a1f8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a1f8-123">Requirement</span></span> | <span data-ttu-id="5a1f8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5a1f8-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1f8-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a1f8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5a1f8-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a1f8-126">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="5a1f8-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a1f8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5a1f8-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a1f8-128">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="5a1f8-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a1f8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a1f8-130"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a1f8-130"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="5a1f8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5a1f8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a1f8-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a1f8-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="5a1f8-133">�</span><span class="sxs-lookup"><span data-stu-id="5a1f8-133">�</span></span>

<span data-ttu-id="5a1f8-134">�</span><span class="sxs-lookup"><span data-stu-id="5a1f8-134">�</span></span>
