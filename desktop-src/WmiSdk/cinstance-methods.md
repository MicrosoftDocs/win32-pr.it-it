---
description: La classe CInstance espone i metodi seguenti.
ms.assetid: B9846350-405D-440E-AC35-16446D3F03F5
ms.tgt_platform: multiple
title: Metodi CInstance
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e088f4604263d3fd1673982e22e2f6c88f991b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883545"
---
# <a name="cinstance-methods"></a><span data-ttu-id="2cd14-103">Metodi CInstance</span><span class="sxs-lookup"><span data-stu-id="2cd14-103">CInstance Methods</span></span>

<span data-ttu-id="2cd14-104">\[La classe [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="2cd14-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="2cd14-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="2cd14-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="2cd14-106">La classe [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="2cd14-106">The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2cd14-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="2cd14-107">In this section</span></span>

-   [<span data-ttu-id="2cd14-108">**Metodo Commit**</span><span class="sxs-lookup"><span data-stu-id="2cd14-108">**Commit method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-commit)
-   [<span data-ttu-id="2cd14-109">**Metodo GetBool**</span><span class="sxs-lookup"><span data-stu-id="2cd14-109">**Getbool method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getbool)
-   [<span data-ttu-id="2cd14-110">**Metodo GetByte**</span><span class="sxs-lookup"><span data-stu-id="2cd14-110">**GetByte method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getbyte)
-   [<span data-ttu-id="2cd14-111">**Metodo GetCHString**</span><span class="sxs-lookup"><span data-stu-id="2cd14-111">**GetCHString method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getchstring)
-   [<span data-ttu-id="2cd14-112">**Metodo GetClassObjectInterface**</span><span class="sxs-lookup"><span data-stu-id="2cd14-112">**GetClassObjectInterface method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getclassobjectinterface)
-   [<span data-ttu-id="2cd14-113">**Metodo GetDateTime**</span><span class="sxs-lookup"><span data-stu-id="2cd14-113">**GetDateTime method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getdatetime)
-   [<span data-ttu-id="2cd14-114">**Metodo GetDouble**</span><span class="sxs-lookup"><span data-stu-id="2cd14-114">**GetDOUBLE method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getdouble)
-   [<span data-ttu-id="2cd14-115">**Metodo getdword**</span><span class="sxs-lookup"><span data-stu-id="2cd14-115">**GetDWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getdword)
-   [<span data-ttu-id="2cd14-116">**Metodo GetEmbeddedObject**</span><span class="sxs-lookup"><span data-stu-id="2cd14-116">**GetEmbeddedObject method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getembeddedobject)
-   [<span data-ttu-id="2cd14-117">**Metodo GetMethodContext**</span><span class="sxs-lookup"><span data-stu-id="2cd14-117">**GetMethodContext method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getmethodcontext)
-   [<span data-ttu-id="2cd14-118">**Metodo GetStatus**</span><span class="sxs-lookup"><span data-stu-id="2cd14-118">**GetStatus method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getstatus)
-   [<span data-ttu-id="2cd14-119">**Metodo GetStringArray**</span><span class="sxs-lookup"><span data-stu-id="2cd14-119">**GetStringArray method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getstringarray)
-   [<span data-ttu-id="2cd14-120">**GetTimeSpan (metodo)**</span><span class="sxs-lookup"><span data-stu-id="2cd14-120">**GetTimeSpan method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-gettimespan)
-   [<span data-ttu-id="2cd14-121">**Metodo getVariant**</span><span class="sxs-lookup"><span data-stu-id="2cd14-121">**GetVariant method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getvariant)
-   [<span data-ttu-id="2cd14-122">**Metodo GetWBEMINT16**</span><span class="sxs-lookup"><span data-stu-id="2cd14-122">**GetWBEMINT16 method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getwbemint16)
-   [<span data-ttu-id="2cd14-123">**Metodi GetWBEMINT64**</span><span class="sxs-lookup"><span data-stu-id="2cd14-123">**GetWBEMINT64 methods**</span></span>](cinstance-getwbemint64.md)
-   [<span data-ttu-id="2cd14-124">**Metodo GetWCHAR**</span><span class="sxs-lookup"><span data-stu-id="2cd14-124">**GetWCHAR method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getwchar)
-   [<span data-ttu-id="2cd14-125">**Metodo getword**</span><span class="sxs-lookup"><span data-stu-id="2cd14-125">**GetWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getword)
-   [<span data-ttu-id="2cd14-126">**Metodo IsNull**</span><span class="sxs-lookup"><span data-stu-id="2cd14-126">**IsNull method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-isnull)
-   [<span data-ttu-id="2cd14-127">**Metodo sebool**</span><span class="sxs-lookup"><span data-stu-id="2cd14-127">**Setbool method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setbool)
-   [<span data-ttu-id="2cd14-128">**Metodo sebyte**</span><span class="sxs-lookup"><span data-stu-id="2cd14-128">**SetByte method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setbyte)
-   [<span data-ttu-id="2cd14-129">**Metodi SetCharSplat**</span><span class="sxs-lookup"><span data-stu-id="2cd14-129">**SetCharSplat methods**</span></span>](cinstance-setcharsplat.md)
-   [<span data-ttu-id="2cd14-130">**Metodi SetCHString**</span><span class="sxs-lookup"><span data-stu-id="2cd14-130">**SetCHString methods**</span></span>](cinstance-setchstring.md)
-   [<span data-ttu-id="2cd14-131">**Metodo sedatetime**</span><span class="sxs-lookup"><span data-stu-id="2cd14-131">**SetDateTime method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setdatetime)
-   [<span data-ttu-id="2cd14-132">**Metodo sedouble**</span><span class="sxs-lookup"><span data-stu-id="2cd14-132">**SetDOUBLE method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setdouble)
-   [<span data-ttu-id="2cd14-133">**Metodo SetValue**</span><span class="sxs-lookup"><span data-stu-id="2cd14-133">**SetDWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setdword)
-   [<span data-ttu-id="2cd14-134">**Metodo SetEmbeddedObject**</span><span class="sxs-lookup"><span data-stu-id="2cd14-134">**SetEmbeddedObject method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setembeddedobject)
-   [<span data-ttu-id="2cd14-135">**Metodo senull**</span><span class="sxs-lookup"><span data-stu-id="2cd14-135">**SetNull method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setnull)
-   [<span data-ttu-id="2cd14-136">**Metodo SetStringArray**</span><span class="sxs-lookup"><span data-stu-id="2cd14-136">**SetStringArray method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setstringarray)
-   [<span data-ttu-id="2cd14-137">**Metodo setimespan**</span><span class="sxs-lookup"><span data-stu-id="2cd14-137">**SetTimeSpan method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-settimespan)
-   [<span data-ttu-id="2cd14-138">**Metodo sevariant**</span><span class="sxs-lookup"><span data-stu-id="2cd14-138">**SetVariant method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setvariant)
-   [<span data-ttu-id="2cd14-139">**Metodo SetWBEMINT16**</span><span class="sxs-lookup"><span data-stu-id="2cd14-139">**SetWBEMINT16 method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setwbemint16)
-   [<span data-ttu-id="2cd14-140">**Metodo SetWCHARSplat**</span><span class="sxs-lookup"><span data-stu-id="2cd14-140">**SetWCHARSplat method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setwcharsplat)
-   <span data-ttu-id="2cd14-141">[**Metodi SetWBEMINT64**](/previous-versions/windows/desktop/legacy/aa389221(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2cd14-141">[**SetWBEMINT64 methods**](/previous-versions/windows/desktop/legacy/aa389221(v=vs.85))</span></span>
-   [<span data-ttu-id="2cd14-142">**Metodo seword**</span><span class="sxs-lookup"><span data-stu-id="2cd14-142">**SetWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setword)

 

 
