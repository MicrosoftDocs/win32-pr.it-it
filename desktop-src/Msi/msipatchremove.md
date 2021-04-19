---
description: La proprietà MSIPATCHREMOVE specifica l'elenco di patch da rimuovere durante un'installazione.
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: Proprietà MSIPATCHREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf83583c5b15311e175e67a867ff5aca71394b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326266"
---
# <a name="msipatchremove-property"></a><span data-ttu-id="12e36-103">Proprietà MSIPATCHREMOVE</span><span class="sxs-lookup"><span data-stu-id="12e36-103">MSIPATCHREMOVE property</span></span>

<span data-ttu-id="12e36-104">La proprietà **MSIPATCHREMOVE** specifica l'elenco di patch da rimuovere durante un'installazione.</span><span class="sxs-lookup"><span data-stu-id="12e36-104">The **MSIPATCHREMOVE** property specifies the list of patches to remove during an installation.</span></span> <span data-ttu-id="12e36-105">Le singole patch nell'elenco sono separate da punti e virgola e possono essere rappresentate dal GUID del codice della patch o dal percorso completo della patch.</span><span class="sxs-lookup"><span data-stu-id="12e36-105">Individual patches in the list are separated by semicolons and can be represented by patch code GUID or the full path to the patch.</span></span> <span data-ttu-id="12e36-106">La funzione [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) e il metodo [**RemovePatches**](installer-removepatches.md) dell'oggetto [Installer](installer-object.md) impostano la proprietà **MSIPATCHREMOVE** .</span><span class="sxs-lookup"><span data-stu-id="12e36-106">The [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) function and the [**RemovePatches**](installer-removepatches.md) method of the [Installer](installer-object.md) object set the **MSIPATCHREMOVE** property.</span></span>

<span data-ttu-id="12e36-107">Per rimuovere una patch, è possibile impostare la proprietà **MSIPATCHREMOVE** nella riga di comando come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="12e36-107">The **MSIPATCHREMOVE** property can be set on the command line as follows to remove a patch.</span></span>

<span data-ttu-id="12e36-108">**msiexec/i A: \\Example.msi MSIPATCHREMOVE = c: \\ patches \\ QFE1. msp; { 0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0}; {A86B443B-E3BF-4009-ADED-F716FC735858}/QB**</span><span class="sxs-lookup"><span data-stu-id="12e36-108">**msiexec /i A:\\Example.msi MSIPATCHREMOVE=c:\\patches\\qfe1.msp;{0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0};{A86B443B-E3BF-4009-ADED-F716FC735858}/qb**</span></span>

## <a name="requirements"></a><span data-ttu-id="12e36-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12e36-109">Requirements</span></span>



| <span data-ttu-id="12e36-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="12e36-110">Requirement</span></span> | <span data-ttu-id="12e36-111">Valore</span><span class="sxs-lookup"><span data-stu-id="12e36-111">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12e36-112">Versione</span><span class="sxs-lookup"><span data-stu-id="12e36-112">Version</span></span><br/> | <span data-ttu-id="12e36-113">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="12e36-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="12e36-114">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="12e36-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="12e36-115">Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="12e36-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="12e36-116">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="12e36-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12e36-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12e36-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e36-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12e36-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="12e36-119">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="12e36-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




