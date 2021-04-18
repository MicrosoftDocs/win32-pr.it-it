---
description: In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta la proprietà MsiNTSuiteEnterprise su 1 se è installato Windows 2000 Advanced Server.
ms.assetid: f5384467-3791-4b0b-a70e-b5343c70db46
title: Proprietà MsiNTSuiteEnterprise
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137b4ece4dbaecdd83b78fd2ce7cfd57820e029d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325168"
---
# <a name="msintsuiteenterprise-property"></a><span data-ttu-id="acd11-103">Proprietà MsiNTSuiteEnterprise</span><span class="sxs-lookup"><span data-stu-id="acd11-103">MsiNTSuiteEnterprise property</span></span>

<span data-ttu-id="acd11-104">In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta la proprietà **MsiNTSuiteEnterprise** su 1 se è installato Windows 2000 Advanced Server.</span><span class="sxs-lookup"><span data-stu-id="acd11-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteEnterprise** property to 1 if Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="acd11-105">Il programma di installazione imposta questa proprietà su 1 solo se \_ il \_ flag Enterprise di ver Suite è impostato nella struttura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="acd11-105">The installer sets this property to 1 only if the VER\_SUITE\_ENTERPRISE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="acd11-106">In caso contrario, il programma di installazione non imposta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="acd11-106">Otherwise, the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="acd11-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="acd11-107">Requirements</span></span>



| <span data-ttu-id="acd11-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="acd11-108">Requirement</span></span> | <span data-ttu-id="acd11-109">Valore</span><span class="sxs-lookup"><span data-stu-id="acd11-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acd11-110">Versione</span><span class="sxs-lookup"><span data-stu-id="acd11-110">Version</span></span><br/> | <span data-ttu-id="acd11-111">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="acd11-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="acd11-112">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="acd11-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="acd11-113">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="acd11-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="acd11-114">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="acd11-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="acd11-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="acd11-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acd11-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="acd11-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
