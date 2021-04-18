---
description: 'Operatore di sottrazione della classe WBEMTime (&\# 8211;) è stato sovraccaricato a:'
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: 'Operatori WBEMTime:: operator-(WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 39256ba9d922ea9d3eef8e442115e840b963ca71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318852"
---
# <a name="wbemtimeoperator--operators"></a><span data-ttu-id="235ae-103">Operatori WBEMTime:: operator-</span><span class="sxs-lookup"><span data-stu-id="235ae-103">WBEMTime::operator- operators</span></span>

<span data-ttu-id="235ae-104">\[La classe [**WBEMTime**](wbemtime.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="235ae-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="235ae-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="235ae-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="235ae-106">L'operatore di sottrazione della classe [**WBEMTime**](wbemtime.md) () è stato sottomesso a overload per:</span><span class="sxs-lookup"><span data-stu-id="235ae-106">The [**WBEMTime**](wbemtime.md) class subtraction operator (�) has been overloaded to:</span></span>

-   <span data-ttu-id="235ae-107">Sottrae un intervallo di tempo dal tempo di un oggetto per produrre un nuovo oggetto temporale che contiene il tempo risultante.</span><span class="sxs-lookup"><span data-stu-id="235ae-107">Subtract a time span from an object's time to produce a new time object that contains the resulting time.</span></span>
-   <span data-ttu-id="235ae-108">Sottrarre un'ora dal tempo dell'oggetto per produrre un nuovo oggetto intervallo di tempo che contiene la differenza tra le due volte.</span><span class="sxs-lookup"><span data-stu-id="235ae-108">Subtract a time from the object's time to produce a new time span object that contains the difference between the two times.</span></span>

### <a name="overload-list"></a><span data-ttu-id="235ae-109">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="235ae-109">Overload list</span></span>



| <span data-ttu-id="235ae-110">Operatore</span><span class="sxs-lookup"><span data-stu-id="235ae-110">Operator</span></span>                                                                         | <span data-ttu-id="235ae-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="235ae-111">Description</span></span>                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="235ae-112">**operatore-(WBEMTime&)**</span><span class="sxs-lookup"><span data-stu-id="235ae-112">**operator-(WBEMTime&)**</span></span>](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | <span data-ttu-id="235ae-113">Sottrae un **WBEMTime** da un **WBEMTime**.</span><span class="sxs-lookup"><span data-stu-id="235ae-113">Subtracts a **WBEMTime** from a **WBEMTime**.</span></span><br/>                         |
| <span data-ttu-id="235ae-114">[**operatore-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_))</span><span class="sxs-lookup"><span data-stu-id="235ae-114">[**operator-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_))</span></span> | <span data-ttu-id="235ae-115">Sottrae un [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) da un **WBEMTime**.</span><span class="sxs-lookup"><span data-stu-id="235ae-115">Subtracts a [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) from a **WBEMTime**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="235ae-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="235ae-116">Requirements</span></span>



| <span data-ttu-id="235ae-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="235ae-117">Requirement</span></span> | <span data-ttu-id="235ae-118">Valore</span><span class="sxs-lookup"><span data-stu-id="235ae-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="235ae-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="235ae-119">Minimum supported client</span></span><br/> | <span data-ttu-id="235ae-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="235ae-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="235ae-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="235ae-121">Minimum supported server</span></span><br/> | <span data-ttu-id="235ae-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="235ae-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="235ae-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="235ae-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="235ae-124"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="235ae-124"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="235ae-125">DLL</span><span class="sxs-lookup"><span data-stu-id="235ae-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="235ae-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="235ae-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="235ae-127">�</span><span class="sxs-lookup"><span data-stu-id="235ae-127">�</span></span>

<span data-ttu-id="235ae-128">�</span><span class="sxs-lookup"><span data-stu-id="235ae-128">�</span></span>
