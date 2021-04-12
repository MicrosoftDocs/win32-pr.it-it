---
description: Gli operatori di assegnazione della classe WBEMTime sono in overload per semplificare le conversioni tra diversi formati di runtime di Windows e ANSI C. Di seguito sono elencate le diverse firme di overload.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: 'Operatori WBEMTime:: operator = (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 637cc76e776060a4c36a12a9b26bd09a6c231a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349611"
---
# <a name="wbemtimeoperator-operators"></a><span data-ttu-id="62f62-104">Operatori WBEMTime:: operator =</span><span class="sxs-lookup"><span data-stu-id="62f62-104">WBEMTime::operator= operators</span></span>

<span data-ttu-id="62f62-105">\[La classe [**WBEMTime**](wbemtime.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="62f62-105">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="62f62-106">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="62f62-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="62f62-107">Gli operatori di assegnazione della classe [**WBEMTime**](wbemtime.md) sono in overload per semplificare le conversioni tra diversi formati di runtime di Windows e ANSI C.</span><span class="sxs-lookup"><span data-stu-id="62f62-107">The [**WBEMTime**](wbemtime.md) class assignment operators are overloaded to facilitate conversions between various Windows and ANSI C run-time time formats.</span></span> <span data-ttu-id="62f62-108">Di seguito sono elencate le diverse firme di overload.</span><span class="sxs-lookup"><span data-stu-id="62f62-108">The various overloaded signatures are listed below.</span></span>

### <a name="overload-list"></a><span data-ttu-id="62f62-109">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="62f62-109">Overload list</span></span>



| <span data-ttu-id="62f62-110">Operatore</span><span class="sxs-lookup"><span data-stu-id="62f62-110">Operator</span></span>                                                                     | <span data-ttu-id="62f62-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62f62-111">Description</span></span>                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span data-ttu-id="62f62-112">[**operatore = (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))</span><span class="sxs-lookup"><span data-stu-id="62f62-112">[**operator=(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))</span></span>               | <span data-ttu-id="62f62-113">Converte un valore **BSTR** nel formato **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="62f62-113">Converts a **BSTR** to **WBEMTime** format.</span></span><br/>         |
| <span data-ttu-id="62f62-114">[**operator = (Time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="62f62-114">[**operator=(time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))</span></span>        | <span data-ttu-id="62f62-115">Converte l' **ora \_ t** nel formato **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="62f62-115">Converts **time\_t** to **WBEMTime** format.</span></span><br/>        |
| <span data-ttu-id="62f62-116">[**operator = (FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="62f62-116">[**operator=(FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span></span>     | <span data-ttu-id="62f62-117">Converte **FILETIME** nel formato **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="62f62-117">Converts **FILETIME** to **WBEMTime** format.</span></span><br/>       |
| <span data-ttu-id="62f62-118">[**operator = (struct TM&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))</span><span class="sxs-lookup"><span data-stu-id="62f62-118">[**operator=(struct tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))</span></span>   | <span data-ttu-id="62f62-119">Converte una struttura **TM** nel formato **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="62f62-119">Converts a **tm** structure to **WBEMTime** format.</span></span><br/> |
| <span data-ttu-id="62f62-120">[**operatore = (SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_))</span><span class="sxs-lookup"><span data-stu-id="62f62-120">[**operator=(SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_))</span></span> | <span data-ttu-id="62f62-121">Converte **SYSTEMTIME** nel formato **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="62f62-121">Converts **SYSTEMTIME** to **WBEMTime** format.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="62f62-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62f62-122">Requirements</span></span>



| <span data-ttu-id="62f62-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="62f62-123">Requirement</span></span> | <span data-ttu-id="62f62-124">Valore</span><span class="sxs-lookup"><span data-stu-id="62f62-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62f62-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62f62-125">Minimum supported client</span></span><br/> | <span data-ttu-id="62f62-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62f62-126">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="62f62-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62f62-127">Minimum supported server</span></span><br/> | <span data-ttu-id="62f62-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62f62-128">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="62f62-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62f62-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="62f62-130"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="62f62-130"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="62f62-131">DLL</span><span class="sxs-lookup"><span data-stu-id="62f62-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62f62-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62f62-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="62f62-133">�</span><span class="sxs-lookup"><span data-stu-id="62f62-133">�</span></span>

<span data-ttu-id="62f62-134">�</span><span class="sxs-lookup"><span data-stu-id="62f62-134">�</span></span>
