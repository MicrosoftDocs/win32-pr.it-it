---
description: Descrive il formato di data e ora Common Information Model (CIM) utilizzato da WMI. Questo formato è indipendente dalle impostazioni locali, quindi gli script che usano DATETIME possono essere eseguiti in molti fusi orari.
ms.assetid: be239bf8-88a3-47bc-ae4f-49a5195e7a7d
ms.tgt_platform: multiple
title: Formato di data e ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e8f97930efa33942fe87b2109aa7cd7ba9d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131159"
---
# <a name="date-and-time-format"></a><span data-ttu-id="59d9c-104">Formato di data e ora</span><span class="sxs-lookup"><span data-stu-id="59d9c-104">Date and Time Format</span></span>

<span data-ttu-id="59d9c-105">WMI usa i formati di data e ora definiti dalla specifica[DMTF.org](https://www.dmtf.org/)(Distributed Management Task Force) Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="59d9c-105">WMI uses the date and time formats defined by the Distributed Management Task Force ([DMTF.org](https://www.dmtf.org/)) Common Information Model (CIM) specification.</span></span>

<span data-ttu-id="59d9c-106">Il **formato \_ DateTime CIM** viene implementato in Microsoft [Managed Object Format (MOF)](managed-object-format--mof-.md) dal tipo di dati MOF [DateTime](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="59d9c-106">The **CIM\_DATETIME** format is implemented in the Microsoft [Managed Object Format (MOF)](managed-object-format--mof-.md) by the [DATETIME](datetime.md) MOF datatype.</span></span> <span data-ttu-id="59d9c-107">I formati di data e ora possono inoltre esprimere un intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="59d9c-107">The date and time formats can also express an interval of time.</span></span>

<span data-ttu-id="59d9c-108">Per ulteriori informazioni sui formati WMI, vedere [CIM \_ DateTime](cim-datetime.md) and [Interval Format](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="59d9c-108">For more information about WMI formats, see [CIM\_DATETIME](cim-datetime.md) and [Interval Format](interval-format.md).</span></span>

<span data-ttu-id="59d9c-109">Per ulteriori informazioni sulla conversione da e verso il formato DATETIME WMI, vedere [**SWbemDateTime**](swbemdatetime.md) e l'articolo su TechNet ScriptCenter [it about time (Oh e about dates)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="59d9c-109">For more information about converting to and from the WMI DATETIME format, see [**SWbemDateTime**](swbemdatetime.md) and the article on TechNet ScriptCenter [It's About Time (Oh, and About Dates, too)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="59d9c-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59d9c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59d9c-111">Informazioni su WMI</span><span class="sxs-lookup"><span data-stu-id="59d9c-111">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 



