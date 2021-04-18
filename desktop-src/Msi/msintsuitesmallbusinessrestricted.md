---
description: In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta la proprietà MsiNTSuiteSmallBusinessRestricted su 1 se Microsoft Small Business Server è installato con la licenza client restrittiva in vigore.
ms.assetid: a7100df4-6fe4-4159-ba94-9b5bd1803107
title: Proprietà MsiNTSuiteSmallBusinessRestricted
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d85fa7fe83c0c8c7cd40788453d1078e7a6b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327182"
---
# <a name="msintsuitesmallbusinessrestricted-property"></a><span data-ttu-id="5a362-103">Proprietà MsiNTSuiteSmallBusinessRestricted</span><span class="sxs-lookup"><span data-stu-id="5a362-103">MsiNTSuiteSmallBusinessRestricted property</span></span>

<span data-ttu-id="5a362-104">In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta la proprietà **MsiNTSuiteSmallBusinessRestricted** su 1 se Microsoft Small Business Server è installato con la licenza client restrittiva in vigore.</span><span class="sxs-lookup"><span data-stu-id="5a362-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteSmallBusinessRestricted** property to 1 if Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="5a362-105">Il programma di installazione imposta questa proprietà su 1 solo se \_ il \_ \_ flag SMALLBUSINESS Restricted di ver Suite è impostato nella struttura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="5a362-105">The installer sets this property to 1 only if the VER\_SUITE\_SMALLBUSINESS\_RESTRICTED flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="5a362-106">In caso contrario, il programma di installazione non imposta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5a362-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a362-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a362-107">Requirements</span></span>



| <span data-ttu-id="5a362-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a362-108">Requirement</span></span> | <span data-ttu-id="5a362-109">Valore</span><span class="sxs-lookup"><span data-stu-id="5a362-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a362-110">Versione</span><span class="sxs-lookup"><span data-stu-id="5a362-110">Version</span></span><br/> | <span data-ttu-id="5a362-111">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5a362-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5a362-112">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a362-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5a362-113">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5a362-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5a362-114">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5a362-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a362-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a362-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a362-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5a362-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
