---
description: In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta la proprietà MsiNTSuiteSmallBusiness su 1 se è installato Microsoft Small Business Server.
ms.assetid: 9ac578b9-316f-413c-aae0-4f414109583b
title: Proprietà MsiNTSuiteSmallBusiness
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d8b1e523ff038e4639cb0f92762c3914bbf5f6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327181"
---
# <a name="msintsuitesmallbusiness-property"></a><span data-ttu-id="ab427-103">Proprietà MsiNTSuiteSmallBusiness</span><span class="sxs-lookup"><span data-stu-id="ab427-103">MsiNTSuiteSmallBusiness property</span></span>

<span data-ttu-id="ab427-104">In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta la proprietà **MsiNTSuiteSmallBusiness** su 1 se è installato Microsoft Small Business Server.</span><span class="sxs-lookup"><span data-stu-id="ab427-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteSmallBusiness** property to 1 if Microsoft Small Business Server is installed.</span></span> <span data-ttu-id="ab427-105">Il programma di installazione imposta questa proprietà su 1 solo se \_ il \_ flag SMALLBUSINESS di ver Suite è impostato nella struttura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="ab427-105">The installer sets this property to 1 only if the VER\_SUITE\_SMALLBUSINESS flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="ab427-106">In caso contrario, il programma di installazione non imposta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="ab427-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab427-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab427-107">Requirements</span></span>



| <span data-ttu-id="ab427-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab427-108">Requirement</span></span> | <span data-ttu-id="ab427-109">Valore</span><span class="sxs-lookup"><span data-stu-id="ab427-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab427-110">Versione</span><span class="sxs-lookup"><span data-stu-id="ab427-110">Version</span></span><br/> | <span data-ttu-id="ab427-111">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ab427-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ab427-112">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ab427-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ab427-113">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ab427-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ab427-114">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ab427-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab427-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab427-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab427-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ab427-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
