---
description: La classe WBEMTimeSpan espone i metodi seguenti.
ms.assetid: 7D450EE2-C52F-4B78-B6B1-9FD74394C3DE
ms.tgt_platform: multiple
title: Metodi WBEMTimeSpan
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d516f22a7ecd5468d53bda44ce47edbe4504d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318844"
---
# <a name="wbemtimespan-methods"></a><span data-ttu-id="6019b-103">Metodi WBEMTimeSpan</span><span class="sxs-lookup"><span data-stu-id="6019b-103">WBEMTimeSpan Methods</span></span>

<span data-ttu-id="6019b-104">\[La classe [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="6019b-104">\[The [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="6019b-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="6019b-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="6019b-106">La classe [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="6019b-106">The [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6019b-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="6019b-107">In this section</span></span>

-   <span data-ttu-id="6019b-108">[**Costruttori WbemTimeSpan**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="6019b-108">[**WbemTimeSpan constructors**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>
-   [<span data-ttu-id="6019b-109">**Clear (metodo)**</span><span class="sxs-lookup"><span data-stu-id="6019b-109">**Clear method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-clear)
-   [<span data-ttu-id="6019b-110">**GetBSTR (metodo)**</span><span class="sxs-lookup"><span data-stu-id="6019b-110">**GetBSTR method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-getbstr)
-   [<span data-ttu-id="6019b-111">**GetTime (metodo)**</span><span class="sxs-lookup"><span data-stu-id="6019b-111">**GetTime method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-gettime)
-   [<span data-ttu-id="6019b-112">**Metodo IsOk**</span><span class="sxs-lookup"><span data-stu-id="6019b-112">**IsOk method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-isok)
-   <span data-ttu-id="6019b-113">[**operator= (metodo)**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="6019b-113">[**operator= method**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span></span>
-   [<span data-ttu-id="6019b-114">**operatore + (metodo)**</span><span class="sxs-lookup"><span data-stu-id="6019b-114">**operator+ method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add)
-   [<span data-ttu-id="6019b-115">**operatore + = (metodo)**</span><span class="sxs-lookup"><span data-stu-id="6019b-115">**operator+= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add-assign)
-   [<span data-ttu-id="6019b-116">**operatore-metodo**</span><span class="sxs-lookup"><span data-stu-id="6019b-116">**operator- method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-sub)
-   [<span data-ttu-id="6019b-117">**operatore-= (metodo)**</span><span class="sxs-lookup"><span data-stu-id="6019b-117">**operator-= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-sub-assign)
-   [<span data-ttu-id="6019b-118">**operatore = = (metodo)**</span><span class="sxs-lookup"><span data-stu-id="6019b-118">**operator == method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-equal-equal-to)
-   [<span data-ttu-id="6019b-119">**operatore! = (metodo)**</span><span class="sxs-lookup"><span data-stu-id="6019b-119">**operator != method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-not-equal-to)
-   [<span data-ttu-id="6019b-120">**operatore > (metodo)**</span><span class="sxs-lookup"><span data-stu-id="6019b-120">**operator > method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)
-   [<span data-ttu-id="6019b-121">**operatore >= (metodo)**</span><span class="sxs-lookup"><span data-stu-id="6019b-121">**operator >= method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)
-   [<span data-ttu-id="6019b-122">**operatore < (metodo)**</span><span class="sxs-lookup"><span data-stu-id="6019b-122">**operator < method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-less-than)
-   [<span data-ttu-id="6019b-123">**operatore <= (metodo)**</span><span class="sxs-lookup"><span data-stu-id="6019b-123">**operator <= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-less-than-equal-to)

 

 
