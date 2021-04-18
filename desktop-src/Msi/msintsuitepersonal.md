---
description: In Windows XP e nei sistemi operativi successivi il programma di installazione imposta la proprietà MsiNTSuitePersonal su 1 se il sistema operativo è Windows XP Home Edition.
ms.assetid: 324a4c45-bd64-4361-90ba-6a0554a9c5ef
title: Proprietà MsiNTSuitePersonal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e8932cf2d2c9c5079d6955571512cbc9836e41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327185"
---
# <a name="msintsuitepersonal-property"></a><span data-ttu-id="04e2b-103">Proprietà MsiNTSuitePersonal</span><span class="sxs-lookup"><span data-stu-id="04e2b-103">MsiNTSuitePersonal property</span></span>

<span data-ttu-id="04e2b-104">In Windows XP e nei sistemi operativi successivi il programma di installazione imposta la proprietà **MsiNTSuitePersonal** su 1 se il sistema operativo è Windows XP Home Edition.</span><span class="sxs-lookup"><span data-stu-id="04e2b-104">On Windows XP and later operating systems, the installer sets the **MsiNTSuitePersonal** property to 1 if the operating system is Windows XP Home Edition.</span></span> <span data-ttu-id="04e2b-105">Il programma di installazione imposta questa proprietà su 1 solo se il flag di VER \_ Suite \_ Personal è impostato nella struttura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="04e2b-105">The installer sets this property to 1 only if the VER\_SUITE\_PERSONAL flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="04e2b-106">In caso contrario, il programma di installazione non imposta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="04e2b-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="04e2b-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04e2b-107">Requirements</span></span>



| <span data-ttu-id="04e2b-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="04e2b-108">Requirement</span></span> | <span data-ttu-id="04e2b-109">Valore</span><span class="sxs-lookup"><span data-stu-id="04e2b-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04e2b-110">Versione</span><span class="sxs-lookup"><span data-stu-id="04e2b-110">Version</span></span><br/> | <span data-ttu-id="04e2b-111">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="04e2b-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="04e2b-112">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="04e2b-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="04e2b-113">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="04e2b-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="04e2b-114">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="04e2b-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="04e2b-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04e2b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04e2b-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="04e2b-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
