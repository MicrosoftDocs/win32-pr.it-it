---
description: Il programma di installazione imposta la proprietà SystemFolder sul percorso completo della cartella di sistema.
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: Proprietà SystemFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abce6e4aa91289ef17134ab3cb878a665d3097c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330144"
---
# <a name="systemfolder-property"></a><span data-ttu-id="e64b0-103">Proprietà SystemFolder</span><span class="sxs-lookup"><span data-stu-id="e64b0-103">SystemFolder property</span></span>

<span data-ttu-id="e64b0-104">Il programma di installazione imposta la proprietà **SystemFolder** sul percorso completo della cartella di sistema.</span><span class="sxs-lookup"><span data-stu-id="e64b0-104">The installer sets the **SystemFolder** property to the full path of the System folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="e64b0-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="e64b0-105">Remarks</span></span>

<span data-ttu-id="e64b0-106">Questa proprietà viene impostata dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="e64b0-106">The installer sets this property.</span></span> <span data-ttu-id="e64b0-107">Ad esempio, in Windows a 32 bit il valore può essere C: \\ Windows \\ system32.</span><span class="sxs-lookup"><span data-stu-id="e64b0-107">For example, on 32-bit Windows the value may be C:\\Windows\\System32.</span></span> <span data-ttu-id="e64b0-108">In Windows a 64 bit il valore può essere C: \\ Windows \\ SysWow64.</span><span class="sxs-lookup"><span data-stu-id="e64b0-108">On 64-bit Windows, the value may be C:\\Windows\\SysWow64.</span></span>

<span data-ttu-id="e64b0-109">Questa cartella è in genere una sottodirectory della cartella Windows.</span><span class="sxs-lookup"><span data-stu-id="e64b0-109">This folder is normally a subdirectory of the Windows folder.</span></span> <span data-ttu-id="e64b0-110">Tuttavia, si trova in un server se configurato per le finestre condivise.</span><span class="sxs-lookup"><span data-stu-id="e64b0-110">However, it resides on a server when configured for Shared Windows.</span></span>

<span data-ttu-id="e64b0-111">Questa cartella è locale, anche se configurata per le finestre condivise.</span><span class="sxs-lookup"><span data-stu-id="e64b0-111">This folder is local, even when configured for shared Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="e64b0-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e64b0-112">Requirements</span></span>



| <span data-ttu-id="e64b0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e64b0-113">Requirement</span></span> | <span data-ttu-id="e64b0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e64b0-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e64b0-115">Versione</span><span class="sxs-lookup"><span data-stu-id="e64b0-115">Version</span></span><br/> | <span data-ttu-id="e64b0-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e64b0-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e64b0-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e64b0-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e64b0-118">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e64b0-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e64b0-119">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e64b0-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e64b0-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e64b0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e64b0-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e64b0-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




