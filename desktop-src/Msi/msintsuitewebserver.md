---
description: In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta la proprietà MsiNTSuiteWebServer su 1 se il programma di installazione è in esecuzione in un'edizione Web di Windows Server 2003.
ms.assetid: de462ba2-4654-4f47-9dd7-3bc9c6f0af0e
title: Proprietà MsiNTSuiteWebServer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 082e3ae7f107bf3499f5a48473d53ebb530138a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327174"
---
# <a name="msintsuitewebserver-property"></a><span data-ttu-id="6ff3f-103">Proprietà MsiNTSuiteWebServer</span><span class="sxs-lookup"><span data-stu-id="6ff3f-103">MsiNTSuiteWebServer property</span></span>

<span data-ttu-id="6ff3f-104">In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta la proprietà **MsiNTSuiteWebServer** su 1 se il programma di installazione è in esecuzione in un'edizione Web di Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6ff3f-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteWebServer** property to 1 if the installer is running on a web edition of the Windows Server 2003.</span></span> <span data-ttu-id="6ff3f-105">Il programma di installazione imposta questa proprietà su 1 solo se il flag del pannello \_ di ver Suite \_ è impostato nella struttura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="6ff3f-105">The installer sets this property to 1 only if the VER\_SUITE\_BLADE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="6ff3f-106">In caso contrario, il programma di installazione non imposta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6ff3f-106">Otherwise the installer does not set this property.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ff3f-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ff3f-107">Remarks</span></span>

<span data-ttu-id="6ff3f-108">Questa proprietà è disponibile solo con la versione di Windows Server 2003 del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="6ff3f-108">This property is available only with the Windows Server 2003 release of the installer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ff3f-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ff3f-109">Requirements</span></span>



| <span data-ttu-id="6ff3f-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ff3f-110">Requirement</span></span> | <span data-ttu-id="6ff3f-111">Valore</span><span class="sxs-lookup"><span data-stu-id="6ff3f-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff3f-112">Versione</span><span class="sxs-lookup"><span data-stu-id="6ff3f-112">Version</span></span><br/> | <span data-ttu-id="6ff3f-113">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6ff3f-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6ff3f-114">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6ff3f-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6ff3f-115">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6ff3f-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6ff3f-116">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="6ff3f-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ff3f-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ff3f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff3f-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6ff3f-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="6ff3f-119">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="6ff3f-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 
