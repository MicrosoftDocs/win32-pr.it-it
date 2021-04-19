---
description: Impostare la proprietà MSIUSEREALADMINDETECTION su 1 per richiedere al programma di installazione di utilizzare le informazioni utente effettive durante l'impostazione della proprietà AdminUser.
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: Proprietà MSIUSEREALADMINDETECTION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0989174f41bc4b58f89e440dd9852dfde6249a5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331067"
---
# <a name="msiuserealadmindetection-property"></a><span data-ttu-id="b35fd-103">Proprietà MSIUSEREALADMINDETECTION</span><span class="sxs-lookup"><span data-stu-id="b35fd-103">MSIUSEREALADMINDETECTION property</span></span>

<span data-ttu-id="b35fd-104">Impostare la proprietà **MSIUSEREALADMINDETECTION** su 1 per richiedere al programma di installazione di utilizzare le informazioni utente effettive durante l'impostazione della proprietà [**AdminUser**](adminuser.md) .</span><span class="sxs-lookup"><span data-stu-id="b35fd-104">Set the **MSIUSEREALADMINDETECTION** property to 1 to request that the installer use actual user information when setting the [**AdminUser**](adminuser.md) property.</span></span> <span data-ttu-id="b35fd-105">Quando è in esecuzione in Windows Vista, i [**privilegi**](privileged.md) e **AdminUser** sono gli stessi.</span><span class="sxs-lookup"><span data-stu-id="b35fd-105">When running on Windows Vista, the [**Privileged**](privileged.md) and **AdminUser** are the same.</span></span> <span data-ttu-id="b35fd-106">Gli autori devono utilizzare la proprietà **Privileged** nei nuovi pacchetti.</span><span class="sxs-lookup"><span data-stu-id="b35fd-106">Authors should used the **Privileged** property in new packages.</span></span> <span data-ttu-id="b35fd-107">I pacchetti legacy che richiedono proprietà con **privilegi** e **AdminUser** distinti possono ripristinare la differenza impostando la proprietà **MSIUSEREALADMINDETECTION** .</span><span class="sxs-lookup"><span data-stu-id="b35fd-107">Legacy packages that require distinct **Privileged** and **AdminUser** properties can restore the difference by setting the **MSIUSEREALADMINDETECTION** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b35fd-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b35fd-108">Requirements</span></span>



| <span data-ttu-id="b35fd-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="b35fd-109">Requirement</span></span> | <span data-ttu-id="b35fd-110">Valore</span><span class="sxs-lookup"><span data-stu-id="b35fd-110">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b35fd-111">Versione</span><span class="sxs-lookup"><span data-stu-id="b35fd-111">Version</span></span><br/> | <span data-ttu-id="b35fd-112">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b35fd-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b35fd-113">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b35fd-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b35fd-114">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b35fd-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b35fd-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b35fd-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b35fd-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b35fd-116">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="b35fd-117">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="b35fd-117">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




