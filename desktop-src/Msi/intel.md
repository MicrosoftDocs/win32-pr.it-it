---
description: La proprietà Intel viene impostata dal Windows Installer al livello di processore numerico durante l'esecuzione in un processore Intel.
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Proprietà Intel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73f35b371d3bf8323fe2a3f3de1608666bc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329748"
---
# <a name="intel-property"></a><span data-ttu-id="25b78-103">Proprietà Intel</span><span class="sxs-lookup"><span data-stu-id="25b78-103">Intel property</span></span>

<span data-ttu-id="25b78-104">La proprietà **Intel** viene impostata dal Windows Installer al livello di processore numerico durante l'esecuzione in un processore Intel.</span><span class="sxs-lookup"><span data-stu-id="25b78-104">The **Intel** property is set by the Windows Installer to the numeric processor level when running on an Intel processor.</span></span> <span data-ttu-id="25b78-105">I valori corrispondono al campo *wProcessorLevel* della struttura delle informazioni di [**sistema \_**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="25b78-105">The values are the same as the *wProcessorLevel* field of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span> <span data-ttu-id="25b78-106">Quando è in esecuzione in un processore x64, il Windows Installer imposta la proprietà **Intel** in modo da riflettere il processore x86 emulato dal computer x64 come riportato dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="25b78-106">When running on a x64 processor, the Windows Installer sets the **Intel** property to reflect the x86 processor emulated by the x64 computer as reported by the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="25b78-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25b78-107">Requirements</span></span>



| <span data-ttu-id="25b78-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="25b78-108">Requirement</span></span> | <span data-ttu-id="25b78-109">Valore</span><span class="sxs-lookup"><span data-stu-id="25b78-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25b78-110">Versione</span><span class="sxs-lookup"><span data-stu-id="25b78-110">Version</span></span><br/> | <span data-ttu-id="25b78-111">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="25b78-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="25b78-112">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="25b78-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="25b78-113">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="25b78-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="25b78-114">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="25b78-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25b78-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25b78-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25b78-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="25b78-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
