---
description: Il metodo GetLocalOffsetForDate restituisce l'offset in minuti (+ o &\# 8211;) tra GMT e l'ora locale per il tempo fornito nell'argomento.
audience: developer
ms.assetid: 15cc5f45-604c-4335-bcd3-92d62dc15420
ms.tgt_platform: multiple
title: 'Metodi WBEMTime:: GetLocalOffsetForDate (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e2c10cd076e18a803f0cb22b2798c09091cc70b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883505"
---
# <a name="wbemtimegetlocaloffsetfordate-methods"></a><span data-ttu-id="7805e-103">Metodi WBEMTime:: GetLocalOffsetForDate</span><span class="sxs-lookup"><span data-stu-id="7805e-103">WBEMTime::GetLocalOffsetForDate methods</span></span>

<span data-ttu-id="7805e-104">\[La classe [**WBEMTime**](wbemtime.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="7805e-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="7805e-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="7805e-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="7805e-106">Il metodo **GetLocalOffsetForDate** restituisce l'offset in minuti (+ o) tra GMT e ora locale per il tempo fornito nell'argomento.</span><span class="sxs-lookup"><span data-stu-id="7805e-106">The **GetLocalOffsetForDate** method returns the offset in minutes (+ or �) between GMT and local time for the time supplied in the argument.</span></span>

### <a name="overload-list"></a><span data-ttu-id="7805e-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="7805e-107">Overload list</span></span>



| <span data-ttu-id="7805e-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="7805e-108">Method</span></span>                                                                                           | <span data-ttu-id="7805e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7805e-109">Description</span></span>                                           |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span data-ttu-id="7805e-110">[**GetLocalOffsetForDate (Time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="7805e-110">[**GetLocalOffsetForDate(time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))</span></span>         | <span data-ttu-id="7805e-111">Argument è un riferimento a un' **ora \_ t**.</span><span class="sxs-lookup"><span data-stu-id="7805e-111">Argument is a reference to a **time\_t**.</span></span><br/>  |
| <span data-ttu-id="7805e-112">[**GetLocalOffsetForDate (FILETIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))</span><span class="sxs-lookup"><span data-stu-id="7805e-112">[**GetLocalOffsetForDate(FILETIME\*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))</span></span>     | <span data-ttu-id="7805e-113">Argument è un puntatore a un oggetto **FILETIME**.</span><span class="sxs-lookup"><span data-stu-id="7805e-113">Argument is a pointer to a **FILETIME**.</span></span><br/>   |
| [<span data-ttu-id="7805e-114">**GetLocalOffsetForDate (struct TM \* )**</span><span class="sxs-lookup"><span data-stu-id="7805e-114">**GetLocalOffsetForDate(struct tm\*)**</span></span>](/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm)   | <span data-ttu-id="7805e-115">Argument è un puntatore alla struttura **TM** .</span><span class="sxs-lookup"><span data-stu-id="7805e-115">Argument is a pointer to **tm** structure.</span></span><br/> |
| <span data-ttu-id="7805e-116">[**GetLocalOffsetForDate (SYSTEMTIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime))</span><span class="sxs-lookup"><span data-stu-id="7805e-116">[**GetLocalOffsetForDate(SYSTEMTIME\*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime))</span></span> | <span data-ttu-id="7805e-117">Argument è un puntatore a un oggetto **SYSTEMTIME**.</span><span class="sxs-lookup"><span data-stu-id="7805e-117">Argument is a pointer to a **SYSTEMTIME**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7805e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7805e-118">Requirements</span></span>



| <span data-ttu-id="7805e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7805e-119">Requirement</span></span> | <span data-ttu-id="7805e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7805e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7805e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7805e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7805e-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7805e-122">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="7805e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7805e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7805e-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7805e-124">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="7805e-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7805e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7805e-126"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="7805e-126"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="7805e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7805e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7805e-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7805e-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="7805e-129">�</span><span class="sxs-lookup"><span data-stu-id="7805e-129">�</span></span>

<span data-ttu-id="7805e-130">�</span><span class="sxs-lookup"><span data-stu-id="7805e-130">�</span></span>
