---
description: Il programma di installazione imposta la proprietà MediaSourceDir su 1 quando l'installazione usa un'origine situata nei supporti, ad esempio un CD-ROM.
ms.assetid: 79c7c5eb-b212-4dbf-943a-00ebd6037ce1
title: Proprietà MediaSourceDir
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ae8ec79d11f8aaf5027ae0e68003532449c52ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327324"
---
# <a name="mediasourcedir-property"></a><span data-ttu-id="66f81-103">Proprietà MediaSourceDir</span><span class="sxs-lookup"><span data-stu-id="66f81-103">MediaSourceDir property</span></span>

<span data-ttu-id="66f81-104">Il programma di installazione imposta la proprietà **MediaSourceDir** su 1 quando l'installazione usa un'origine situata nei supporti, ad esempio un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="66f81-104">The installer sets the **MediaSourceDir** property to 1 when the installation uses a source located on media, such as a CD-ROM.</span></span> <span data-ttu-id="66f81-105">Questa proprietà non viene impostata quando l'installazione usa un'origine che si trova in un percorso di rete.</span><span class="sxs-lookup"><span data-stu-id="66f81-105">This property is not set when the installation uses a source located at a network location.</span></span> <span data-ttu-id="66f81-106">Ad esempio, il [controllo SelectionTree](selectiontree-control.md) USA **MediaSourceDir** per determinare se l'installazione viene eseguita dall'origine o da un percorso di rete.</span><span class="sxs-lookup"><span data-stu-id="66f81-106">For example, the [SelectionTree Control](selectiontree-control.md) uses **MediaSourceDir** to determine whether the installation is being run from source or run from a network location.</span></span>

## <a name="requirements"></a><span data-ttu-id="66f81-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66f81-107">Requirements</span></span>



| <span data-ttu-id="66f81-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="66f81-108">Requirement</span></span> | <span data-ttu-id="66f81-109">Valore</span><span class="sxs-lookup"><span data-stu-id="66f81-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66f81-110">Versione</span><span class="sxs-lookup"><span data-stu-id="66f81-110">Version</span></span><br/> | <span data-ttu-id="66f81-111">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="66f81-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="66f81-112">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="66f81-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="66f81-113">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="66f81-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="66f81-114">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="66f81-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66f81-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66f81-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f81-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="66f81-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 




