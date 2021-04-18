---
description: Il programma di installazione imposta la proprietà RedirectedDLLSupport se la piattaforma di sistema che esegue l'installazione supporta componenti isolati.
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: Proprietà RedirectedDLLSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed308eaf022ada5c6c8697ba47f55605f1fecbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328759"
---
# <a name="redirecteddllsupport-property"></a><span data-ttu-id="93053-103">Proprietà RedirectedDLLSupport</span><span class="sxs-lookup"><span data-stu-id="93053-103">RedirectedDLLSupport property</span></span>

<span data-ttu-id="93053-104">Il programma di installazione imposta la proprietà **RedirectedDLLSupport** se la piattaforma di sistema che esegue l'installazione supporta [componenti isolati](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="93053-104">The installer sets the **RedirectedDLLSupport** property if the system platform performing the installation supports [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="93053-105">Il programma di installazione imposta la proprietà **RedirectedDLLSupport** su un valore pari a 1 se il sistema che esegue l'installazione supporta [componenti isolati](isolated-components.md) basati su. File locali.</span><span class="sxs-lookup"><span data-stu-id="93053-105">The installer sets the **RedirectedDLLSupport** property to a value of 1 if the system performing the installation supports [Isolated Components](isolated-components.md) based on .LOCAL files.</span></span> <span data-ttu-id="93053-106">Il programma di installazione imposta la proprietà **RedirectedDLLSupport** su un valore pari a 2 Se il sistema che esegue l'installazione supporta l'isolamento tramite. File locali o assembly side-by-side Win32.</span><span class="sxs-lookup"><span data-stu-id="93053-106">The installer sets the **RedirectedDLLSupport** property to a value of 2 if the system that performs the installation supports isolation using either .LOCAL files or Win32 side-by-side assemblies.</span></span>

<span data-ttu-id="93053-107">È possibile utilizzare la proprietà **RedirectedDLLSupport** per condizionare l' [azione IsolateComponents](isolatecomponents-action.md) nella tabella [InstallUISequence](installuisequence-table.md) o [InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="93053-107">The **RedirectedDLLSupport** property can be used to condition the [IsolateComponents action](isolatecomponents-action.md) in the [InstallUISequence table](installuisequence-table.md) or [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93053-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93053-108">Requirements</span></span>



| <span data-ttu-id="93053-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="93053-109">Requirement</span></span> | <span data-ttu-id="93053-110">Valore</span><span class="sxs-lookup"><span data-stu-id="93053-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93053-111">Versione</span><span class="sxs-lookup"><span data-stu-id="93053-111">Version</span></span><br/> | <span data-ttu-id="93053-112">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="93053-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="93053-113">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="93053-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="93053-114">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="93053-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="93053-115">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="93053-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93053-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93053-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93053-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="93053-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




