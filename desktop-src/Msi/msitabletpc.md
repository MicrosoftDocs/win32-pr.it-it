---
description: Il programma di installazione imposta la proprietà MsiTabletPC su un valore diverso da zero se il sistema operativo corrente è Windows XP Tablet PC Edition.
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: Proprietà MsiTabletPC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf2878dbaa895e0924a50900d331db0b879edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331075"
---
# <a name="msitabletpc-property"></a><span data-ttu-id="ecbca-103">Proprietà MsiTabletPC</span><span class="sxs-lookup"><span data-stu-id="ecbca-103">MsiTabletPC property</span></span>

<span data-ttu-id="ecbca-104">Il programma di installazione imposta la proprietà **MsiTabletPC** su un valore diverso da zero se il sistema operativo corrente è Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="ecbca-104">The installer sets the **MsiTabletPC** property to a nonzero value if the current operating system is Windows XP Tablet PC Edition.</span></span> <span data-ttu-id="ecbca-105">Il programma di installazione utilizza la funzione [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con **SM \_ TABLETPC** e la proprietà riceve il valore diverso da zero restituito da questa funzione.</span><span class="sxs-lookup"><span data-stu-id="ecbca-105">The installer uses the [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function with **SM\_TABLETPC**, and the property receives the nonzero value returned by this function.</span></span> <span data-ttu-id="ecbca-106">Se il sistema corrente non è Windows XP Tablet PC Edition, la funzione **GetSystemMetrics** restituisce zero e il programma di installazione non imposta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="ecbca-106">If the current system is not Windows XP Tablet PC Edition, the **GetSystemMetrics** function returns zero and the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecbca-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecbca-107">Requirements</span></span>



| <span data-ttu-id="ecbca-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecbca-108">Requirement</span></span> | <span data-ttu-id="ecbca-109">Valore</span><span class="sxs-lookup"><span data-stu-id="ecbca-109">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecbca-110">Versione</span><span class="sxs-lookup"><span data-stu-id="ecbca-110">Version</span></span><br/> | <span data-ttu-id="ecbca-111">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ecbca-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ecbca-112">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ecbca-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ecbca-113">Windows Installer 4,5 in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ecbca-113">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ecbca-114">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbca-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ecbca-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecbca-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecbca-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ecbca-116">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="ecbca-117">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="ecbca-117">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
