---
description: Il Windows Installer imposta la proprietà OriginalDatabase sul percorso del database di installazione utilizzato per avviare l'installazione.
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: Proprietà OriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 592bc86a9ef53602f686e48b3c98dad17a49cfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327802"
---
# <a name="originaldatabase-property"></a><span data-ttu-id="a0508-103">Proprietà OriginalDatabase</span><span class="sxs-lookup"><span data-stu-id="a0508-103">OriginalDatabase property</span></span>

<span data-ttu-id="a0508-104">Il Windows Installer imposta la proprietà **OriginalDatabase** sul percorso del database di installazione utilizzato per avviare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="a0508-104">The Windows Installer sets the **OriginalDatabase** property to the path of the installation database used to launch the installation.</span></span> <span data-ttu-id="a0508-105">Se l'installazione viene avviata da una riga di comando, il valore varia a seconda che l'opzione di recaching Package (il flag-v) sia presente nella proprietà [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="a0508-105">If the installation is launched from a command line, the value depends on whether the recache package option (the -v flag) is present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>



| <span data-ttu-id="a0508-106">Metodo di installazione</span><span class="sxs-lookup"><span data-stu-id="a0508-106">Installation Method</span></span>                                                                                                                                                                                  | <span data-ttu-id="a0508-107">Valore OriginalDatabase</span><span class="sxs-lookup"><span data-stu-id="a0508-107">OriginalDatabase Value</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="a0508-108">Qualsiasi installazione avviata richiamando il percorso del pacchetto di installazione (file MSI).</span><span class="sxs-lookup"><span data-stu-id="a0508-108">Any installation launched by invoking the path of the installation package (.msi file).</span></span>                                                                                                              | <span data-ttu-id="a0508-109">Percorso del pacchetto di installazione (file MSI).</span><span class="sxs-lookup"><span data-stu-id="a0508-109">Path to the installation package (.msi file).</span></span> |
| <span data-ttu-id="a0508-110">Installazione avviata da una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="a0508-110">Installation launched from a command line.</span></span> <span data-ttu-id="a0508-111">L'installazione non è stata avviata da un percorso del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a0508-111">The installation is not launched from a package path.</span></span> <span data-ttu-id="a0508-112">L'opzione recache (flag-v) è presente nella proprietà [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="a0508-112">The recache option (-v flag) is present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>     | <span data-ttu-id="a0508-113">Percorso del database nell'origine.</span><span class="sxs-lookup"><span data-stu-id="a0508-113">Path to the database on the source.</span></span>           |
| <span data-ttu-id="a0508-114">Installazione avviata da una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="a0508-114">Installation launched from a command line.</span></span> <span data-ttu-id="a0508-115">L'installazione non è stata avviata da un percorso del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a0508-115">The installation is not launched from a package path.</span></span> <span data-ttu-id="a0508-116">L'opzione recache (flag-v) non è presente nella proprietà [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="a0508-116">The recache option (-v flag) is not present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> | <span data-ttu-id="a0508-117">Percorso del database memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="a0508-117">Path to the cached database.</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="a0508-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0508-118">Remarks</span></span>

<span data-ttu-id="a0508-119">Durante la prima installazione, un'azione personalizzata sequenziata prima dell' [azione ResolveSource](resolvesource-action.md) può utilizzare la proprietà **OriginalDatabase** per determinare il percorso dell'origine di installazione.</span><span class="sxs-lookup"><span data-stu-id="a0508-119">During a first time installation, a custom action sequenced before the [ResolveSource action](resolvesource-action.md) can use the **OriginalDatabase** property to determine the location of the installation source.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0508-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0508-120">Requirements</span></span>



| <span data-ttu-id="a0508-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0508-121">Requirement</span></span> | <span data-ttu-id="a0508-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a0508-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0508-123">Versione</span><span class="sxs-lookup"><span data-stu-id="a0508-123">Version</span></span><br/> | <span data-ttu-id="a0508-124">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a0508-124">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a0508-125">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a0508-125">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a0508-126">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a0508-126">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a0508-127">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a0508-127">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a0508-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0508-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0508-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a0508-129">Properties</span></span>](properties.md)
</dt> </dl>

 

 




