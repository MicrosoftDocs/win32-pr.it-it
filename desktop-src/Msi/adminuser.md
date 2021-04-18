---
description: Il programma di installazione imposta questa proprietà se l'utente dispone di privilegi di amministratore.
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: Proprietà AdminUser
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11651f0d7103edabbcf7b40087db91f999b1a5b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333678"
---
# <a name="adminuser-property"></a><span data-ttu-id="83ce1-103">Proprietà AdminUser</span><span class="sxs-lookup"><span data-stu-id="83ce1-103">AdminUser property</span></span>

<span data-ttu-id="83ce1-104">Il programma di installazione imposta questa proprietà se l'utente dispone di privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="83ce1-104">The installer sets this property if the user has administrator privileges.</span></span>

<span data-ttu-id="83ce1-105">**Windows Server 2008 e Windows Vista:** La proprietà **AdminUser** è uguale alla proprietà [**Privileged**](privileged.md) .</span><span class="sxs-lookup"><span data-stu-id="83ce1-105">**Windows Server 2008 and Windows Vista:** The **AdminUser** property is the same as the [**Privileged**](privileged.md) property.</span></span> <span data-ttu-id="83ce1-106">Gli autori devono utilizzare la proprietà **Privileged** .</span><span class="sxs-lookup"><span data-stu-id="83ce1-106">Authors should used the **Privileged** property.</span></span> <span data-ttu-id="83ce1-107">Queste proprietà vengono impostate dal programma di installazione se l'utente dispone dei privilegi di amministratore, se l'applicazione è stata assegnata da un amministratore di sistema o se i criteri utente e computer AlwaysInstallElevated sono impostati su true.</span><span class="sxs-lookup"><span data-stu-id="83ce1-107">The installer sets these properties if the user has administrator privileges, if the application has been assigned by a system administrator, or if both the user and machine policies AlwaysInstallElevated are set to true.</span></span>

## <a name="remarks"></a><span data-ttu-id="83ce1-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="83ce1-108">Remarks</span></span>

<span data-ttu-id="83ce1-109">È possibile che le differenze tra queste proprietà siano state utilizzate in alcuni pacchetti legacy.</span><span class="sxs-lookup"><span data-stu-id="83ce1-109">The differences between these properties may have been used in some legacy packages.</span></span> <span data-ttu-id="83ce1-110">Ad esempio, è possibile che sia stato usato **AdminUser** anziché [**Privileged**](privileged.md) nelle istruzioni condizionali, perché il programma di installazione imposta solo la proprietà **AdminUser** se l'utente è un amministratore.</span><span class="sxs-lookup"><span data-stu-id="83ce1-110">For example, **AdminUser** may have been used instead of [**Privileged**](privileged.md) in conditional statements, because the installer only sets the **AdminUser** property if the user is an administrator.</span></span> <span data-ttu-id="83ce1-111">Il programma di installazione imposta la proprietà **Privileged** se l'utente è un amministratore o se Policy consente all'utente di eseguire l'installazione con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="83ce1-111">The installer sets the **Privileged** property if the user is an administrator, or if policy enables the user to install with elevated privileges.</span></span>

<span data-ttu-id="83ce1-112">**Windows Server 2008 e Windows Vista:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="83ce1-112">**Windows Server 2008 and Windows Vista:** Not supported.</span></span> <span data-ttu-id="83ce1-113">[**Privileged**](privileged.md) e **AdminUser** sono uguali.</span><span class="sxs-lookup"><span data-stu-id="83ce1-113">The [**Privileged**](privileged.md) and **AdminUser** are the same.</span></span> <span data-ttu-id="83ce1-114">I pacchetti che richiedono proprietà con **privilegi** e **AdminUser** distinti possono ripristinare la differenza impostando la proprietà [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) .</span><span class="sxs-lookup"><span data-stu-id="83ce1-114">Packages that require distinct **Privileged** and **AdminUser** properties can restore the difference by setting the [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) property.</span></span>

<span data-ttu-id="83ce1-115">Per ulteriori informazioni, vedere [installazione di un pacchetto con privilegi elevati per una proprietà non amministratore](installing-a-package-with-elevated-privileges-for-a-non-admin.md)e [**privilegiata**](privileged.md) .</span><span class="sxs-lookup"><span data-stu-id="83ce1-115">For more information, see [Installing a Package with Elevated Privileges for a Non-Admin](installing-a-package-with-elevated-privileges-for-a-non-admin.md), and [**Privileged**](privileged.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="83ce1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83ce1-116">Requirements</span></span>



| <span data-ttu-id="83ce1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="83ce1-117">Requirement</span></span> | <span data-ttu-id="83ce1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="83ce1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83ce1-119">Versione</span><span class="sxs-lookup"><span data-stu-id="83ce1-119">Version</span></span><br/> | <span data-ttu-id="83ce1-120">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="83ce1-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="83ce1-121">Windows Installer 4,0 o Windows Installer 4,5 in Windows Vista o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="83ce1-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="83ce1-122">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="83ce1-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="83ce1-123">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="83ce1-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83ce1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83ce1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83ce1-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="83ce1-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




