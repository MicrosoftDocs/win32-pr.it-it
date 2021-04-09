---
description: La classe CHString espone i metodi seguenti.
ms.assetid: C064D6DE-14C4-4143-8164-B367C10CBF8E
ms.tgt_platform: multiple
title: Metodi CHString
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15a26bf2b5945990f8cd37ee67c2953395ca98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050232"
---
# <a name="chstring-methods"></a><span data-ttu-id="24081-103">Metodi CHString</span><span class="sxs-lookup"><span data-stu-id="24081-103">CHString Methods</span></span>

<span data-ttu-id="24081-104">\[La classe [**CHString**](chstring.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="24081-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="24081-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="24081-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="24081-106">La classe [**CHString**](chstring.md) espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="24081-106">The [**CHString**](chstring.md) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="24081-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="24081-107">In this section</span></span>

-   [<span data-ttu-id="24081-108">**Metodo AllocSysString**</span><span class="sxs-lookup"><span data-stu-id="24081-108">**AllocSysString method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)
-   <span data-ttu-id="24081-109">[**Costruttori CHString**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))</span><span class="sxs-lookup"><span data-stu-id="24081-109">[**CHString constructors**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))</span></span>
-   [<span data-ttu-id="24081-110">**Metodo COLLATE**</span><span class="sxs-lookup"><span data-stu-id="24081-110">**Collate method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-collate)
-   [<span data-ttu-id="24081-111">**Compare (metodo)**</span><span class="sxs-lookup"><span data-stu-id="24081-111">**Compare method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-compare)
-   [<span data-ttu-id="24081-112">**Metodo CompareNoCase**</span><span class="sxs-lookup"><span data-stu-id="24081-112">**CompareNoCase method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)
-   [<span data-ttu-id="24081-113">**Metodo Empty**</span><span class="sxs-lookup"><span data-stu-id="24081-113">**Empty method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-empty)
-   <span data-ttu-id="24081-114">[**Metodi Find**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))</span><span class="sxs-lookup"><span data-stu-id="24081-114">[**Find methods**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))</span></span>
-   [<span data-ttu-id="24081-115">**Metodo FindOneOf**</span><span class="sxs-lookup"><span data-stu-id="24081-115">**FindOneOf method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)
-   <span data-ttu-id="24081-116">[**Metodi Format**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))</span><span class="sxs-lookup"><span data-stu-id="24081-116">[**Format methods**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))</span></span>
-   <span data-ttu-id="24081-117">[**Metodi FormatMessageW**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))</span><span class="sxs-lookup"><span data-stu-id="24081-117">[**FormatMessageW methods**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))</span></span>
-   [<span data-ttu-id="24081-118">**Metodo FormatV**</span><span class="sxs-lookup"><span data-stu-id="24081-118">**FormatV method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)
-   [<span data-ttu-id="24081-119">**Metodo FreeExtra**</span><span class="sxs-lookup"><span data-stu-id="24081-119">**FreeExtra method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)
-   [<span data-ttu-id="24081-120">**Metodo GetAllocLength**</span><span class="sxs-lookup"><span data-stu-id="24081-120">**GetAllocLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)
-   <span data-ttu-id="24081-121">[**Metodo GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))</span><span class="sxs-lookup"><span data-stu-id="24081-121">[**GetAt method**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))</span></span>
-   [<span data-ttu-id="24081-122">**GetBuffer (metodo)**</span><span class="sxs-lookup"><span data-stu-id="24081-122">**GetBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)
-   [<span data-ttu-id="24081-123">**Metodo GetBufferSetLength**</span><span class="sxs-lookup"><span data-stu-id="24081-123">**GetBufferSetLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength)
-   [<span data-ttu-id="24081-124">**GetData (metodo)**</span><span class="sxs-lookup"><span data-stu-id="24081-124">**GetData method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)
-   [<span data-ttu-id="24081-125">**Metodo GetLength**</span><span class="sxs-lookup"><span data-stu-id="24081-125">**GetLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)
-   [<span data-ttu-id="24081-126">**IsEmpty (metodo)**</span><span class="sxs-lookup"><span data-stu-id="24081-126">**IsEmpty method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)
-   [<span data-ttu-id="24081-127">**Left (metodo)**</span><span class="sxs-lookup"><span data-stu-id="24081-127">**Left method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-left)
-   <span data-ttu-id="24081-128">[**Metodo LoadStringW**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))</span><span class="sxs-lookup"><span data-stu-id="24081-128">[**LoadStringW method**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))</span></span>
-   [<span data-ttu-id="24081-129">**Metodo LockBuffer**</span><span class="sxs-lookup"><span data-stu-id="24081-129">**LockBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)
-   [<span data-ttu-id="24081-130">**Metodo MakeLower**</span><span class="sxs-lookup"><span data-stu-id="24081-130">**MakeLower method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)
-   [<span data-ttu-id="24081-131">**Metodo MakeReverse**</span><span class="sxs-lookup"><span data-stu-id="24081-131">**MakeReverse method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)
-   [<span data-ttu-id="24081-132">**Metodo MakeUpper**</span><span class="sxs-lookup"><span data-stu-id="24081-132">**MakeUpper method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)
-   <span data-ttu-id="24081-133">[**Metodi Mid**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span><span class="sxs-lookup"><span data-stu-id="24081-133">[**Mid methods**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span></span>
-   <span data-ttu-id="24081-134">[**operatore ( \[ \] metodo)**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24081-134">[**operator\[\] method**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))</span></span>
-   [<span data-ttu-id="24081-135">**CHString:: operator +**</span><span class="sxs-lookup"><span data-stu-id="24081-135">**CHString::operator+**</span></span>](chstring--operator-plus.md)
-   [<span data-ttu-id="24081-136">**CHString:: operator + =**</span><span class="sxs-lookup"><span data-stu-id="24081-136">**CHString::operator+=**</span></span>](chstring--operator-plus-equal.md)
-   [<span data-ttu-id="24081-137">**CHString:: operator =**</span><span class="sxs-lookup"><span data-stu-id="24081-137">**CHString::operator=**</span></span>](chstring--operator-equal.md)
-   <span data-ttu-id="24081-138">[**operator = = (constCHString&, constCHString&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24081-138">[**operator==(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))</span></span>
-   <span data-ttu-id="24081-139">[**operator = = (constCHString&, constLPCWSTR&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24081-139">[**operator==(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))</span></span>
-   <span data-ttu-id="24081-140">[**operatore> (constCHString&, constCHString&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24081-140">[**operator>(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))</span></span>
-   <span data-ttu-id="24081-141">[**operatore> (constCHString&, constLPCWSTR&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24081-141">[**operator>(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))</span></span>
-   <span data-ttu-id="24081-142">[**operatore>= (constCHString&, constCHString&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24081-142">[**operator>=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))</span></span>
-   <span data-ttu-id="24081-143">[**operatore>= (constCHString&, constLPCWSTR&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24081-143">[**operator>=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))</span></span>
-   <span data-ttu-id="24081-144">[**operatore< (constCHString&, constCHString&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24081-144">[**operator<(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))</span></span>
-   <span data-ttu-id="24081-145">[**operatore< (constCHString&, constLPCWSTR&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24081-145">[**operator<(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))</span></span>
-   <span data-ttu-id="24081-146">[**operatore<= (constCHString&, constCHString&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24081-146">[**operator<=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))</span></span>
-   <span data-ttu-id="24081-147">[**operatore<= (constCHString&, constLPCWSTR&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24081-147">[**operator<=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))</span></span>
-   <span data-ttu-id="24081-148">[**operator! = (constCHString&, constCHString&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24081-148">[**operator!=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))</span></span>
-   <span data-ttu-id="24081-149">[**operator! = (constCHString&, constLPCWSTR&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24081-149">[**operator!=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))</span></span>
-   [<span data-ttu-id="24081-150">**operatore LPCWSTR (metodo)**</span><span class="sxs-lookup"><span data-stu-id="24081-150">**operator LPCWSTR method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)
-   [<span data-ttu-id="24081-151">**Metodo ReleaseBuffer**</span><span class="sxs-lookup"><span data-stu-id="24081-151">**ReleaseBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)
-   [<span data-ttu-id="24081-152">**Metodo ReverseFind**</span><span class="sxs-lookup"><span data-stu-id="24081-152">**ReverseFind method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)
-   [<span data-ttu-id="24081-153">**Metodo Right**</span><span class="sxs-lookup"><span data-stu-id="24081-153">**Right method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-right)
-   [<span data-ttu-id="24081-154">**Metodo SetAt**</span><span class="sxs-lookup"><span data-stu-id="24081-154">**SetAt method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-setat)
-   [<span data-ttu-id="24081-155">**Metodo SpanExcluding**</span><span class="sxs-lookup"><span data-stu-id="24081-155">**SpanExcluding method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)
-   [<span data-ttu-id="24081-156">**Metodo SpanIncluding**</span><span class="sxs-lookup"><span data-stu-id="24081-156">**SpanIncluding method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)
-   [<span data-ttu-id="24081-157">**Metodo TrimLeft**</span><span class="sxs-lookup"><span data-stu-id="24081-157">**TrimLeft method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)
-   [<span data-ttu-id="24081-158">**Metodo TrimRight**</span><span class="sxs-lookup"><span data-stu-id="24081-158">**TrimRight method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)
-   [<span data-ttu-id="24081-159">**Metodo UnlockBuffer**</span><span class="sxs-lookup"><span data-stu-id="24081-159">**UnlockBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)

 

 
