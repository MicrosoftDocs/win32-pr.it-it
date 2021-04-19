---
description: In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta la proprietà MsiNTSuiteBackOffice su 1 se sono installati i componenti di Microsoft BackOffice.
ms.assetid: 31493732-3082-4dd9-9a20-21658f53c8c2
title: Proprietà MsiNTSuiteBackOffice
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2d9f2f1d95446c32b4f2addf520f3d5b4dadc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332612"
---
# <a name="msintsuitebackoffice-property"></a><span data-ttu-id="f0764-103">Proprietà MsiNTSuiteBackOffice</span><span class="sxs-lookup"><span data-stu-id="f0764-103">MsiNTSuiteBackOffice property</span></span>

<span data-ttu-id="f0764-104">In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta la proprietà **MsiNTSuiteBackOffice** su 1 se sono installati i componenti di Microsoft BackOffice.</span><span class="sxs-lookup"><span data-stu-id="f0764-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteBackOffice** property to 1 if Microsoft BackOffice components are installed.</span></span> <span data-ttu-id="f0764-105">Il programma di installazione imposta questa proprietà su 1 solo se \_ il \_ flag di versione BackOffice di ver Suite è impostato nella struttura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="f0764-105">The installer sets this property to 1 only if the VER\_SUITE\_BACKOFFICE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="f0764-106">In caso contrario, il programma di installazione non imposta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="f0764-106">Otherwise, the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0764-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0764-107">Requirements</span></span>



| <span data-ttu-id="f0764-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0764-108">Requirement</span></span> | <span data-ttu-id="f0764-109">Valore</span><span class="sxs-lookup"><span data-stu-id="f0764-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0764-110">Versione</span><span class="sxs-lookup"><span data-stu-id="f0764-110">Version</span></span><br/> | <span data-ttu-id="f0764-111">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f0764-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f0764-112">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f0764-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f0764-113">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f0764-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f0764-114">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f0764-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f0764-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0764-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0764-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f0764-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
