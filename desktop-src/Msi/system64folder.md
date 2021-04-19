---
description: Il programma di installazione imposta la proprietà System64Folder sul percorso completo della cartella system64 predefinita. La proprietà System64Folder esistente è impostata sulla cartella a 32 bit corrispondente.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: Proprietà System64Folder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e05f9067c4f5a77b5361fdefe0f5b47b9116ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332934"
---
# <a name="system64folder-property"></a><span data-ttu-id="6078b-104">Proprietà System64Folder</span><span class="sxs-lookup"><span data-stu-id="6078b-104">System64Folder property</span></span>

<span data-ttu-id="6078b-105">Il programma di installazione imposta la proprietà **System64Folder** sul percorso completo della cartella system64 predefinita.</span><span class="sxs-lookup"><span data-stu-id="6078b-105">The installer sets the **System64Folder** property to the full path to the predefined System64 folder.</span></span> <span data-ttu-id="6078b-106">La proprietà **System64Folder** esistente è impostata sulla cartella a 32 bit corrispondente.</span><span class="sxs-lookup"><span data-stu-id="6078b-106">The existing **System64Folder** property is set to the corresponding 32-bit folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="6078b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="6078b-107">Remarks</span></span>

<span data-ttu-id="6078b-108">Il programma di installazione imposta questa proprietà su Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="6078b-108">The installer sets this property on 64-bit Windows.</span></span> <span data-ttu-id="6078b-109">Ad esempio, in Windows a 64 bit, il valore può essere C: \\ Window \\ system32.</span><span class="sxs-lookup"><span data-stu-id="6078b-109">For example, on 64-bit Windows, the value may be C:\\Window\\System32.</span></span> <span data-ttu-id="6078b-110">Questa proprietà non viene utilizzata in Windows a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="6078b-110">This property is not used on 32-bit Windows.</span></span>

<span data-ttu-id="6078b-111">Questa cartella è in genere una sottodirectory della cartella Windows.</span><span class="sxs-lookup"><span data-stu-id="6078b-111">This folder is normally a subdirectory of the Windows folder.</span></span> <span data-ttu-id="6078b-112">Tuttavia, si trova in un server se configurato per le finestre condivise.</span><span class="sxs-lookup"><span data-stu-id="6078b-112">However, it resides on a server when configured for Shared Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="6078b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6078b-113">Requirements</span></span>



| <span data-ttu-id="6078b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6078b-114">Requirement</span></span> | <span data-ttu-id="6078b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6078b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6078b-116">Versione</span><span class="sxs-lookup"><span data-stu-id="6078b-116">Version</span></span><br/> | <span data-ttu-id="6078b-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6078b-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6078b-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6078b-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6078b-119">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6078b-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6078b-120">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="6078b-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6078b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6078b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6078b-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6078b-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




