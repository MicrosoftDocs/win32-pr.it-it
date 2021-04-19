---
description: La proprietà PatchFiles restituisce un oggetto String List contenente un elenco di file che possono essere aggiornati dall'elenco di patch fornito.
ms.assetid: 14549847-8558-4a9a-9ad5-3575c3f4391e
title: Proprietà Installer. PatchFiles
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchFiles
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 43491bb384e6f95b31b4e7ae12e5fd32f4fbe8b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332955"
---
# <a name="installerpatchfiles-property"></a><span data-ttu-id="2e29c-103">Proprietà Installer. PatchFiles</span><span class="sxs-lookup"><span data-stu-id="2e29c-103">Installer.PatchFiles property</span></span>

<span data-ttu-id="2e29c-104">La proprietà **PatchFiles** restituisce un oggetto [**String**](stringlist-object.md) List contenente un elenco di file che possono essere aggiornati dall'elenco di patch fornito.</span><span class="sxs-lookup"><span data-stu-id="2e29c-104">The **PatchFiles** property returns a [**StringList**](stringlist-object.md) object that contains a list of files that can be updated by the provided list of patches.</span></span> <span data-ttu-id="2e29c-105">Questa proprietà chiama [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span><span class="sxs-lookup"><span data-stu-id="2e29c-105">This property calls [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span></span> <span data-ttu-id="2e29c-106">Per ulteriori informazioni sull'utilizzo della proprietà **PatchFiles** , vedere [l'elenco dei file che è possibile aggiornare](listing-the-files-that-can-be-updated.md).</span><span class="sxs-lookup"><span data-stu-id="2e29c-106">For more information about using the **PatchFiles** property see [Listing the Files that can be Updated](listing-the-files-that-can-be-updated.md).</span></span>

<span data-ttu-id="2e29c-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2e29c-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e29c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e29c-108">Syntax</span></span>


```JScript
propVal = Installer.PatchFiles
```



## <a name="property-value"></a><span data-ttu-id="2e29c-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2e29c-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="2e29c-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e29c-110">Requirements</span></span>



| <span data-ttu-id="2e29c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e29c-111">Requirement</span></span> | <span data-ttu-id="2e29c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="2e29c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e29c-113">Versione</span><span class="sxs-lookup"><span data-stu-id="2e29c-113">Version</span></span><br/> | <span data-ttu-id="2e29c-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2e29c-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2e29c-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2e29c-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2e29c-116">Windows Installer 4,5 in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="2e29c-116">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="2e29c-117">DLL</span><span class="sxs-lookup"><span data-stu-id="2e29c-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="2e29c-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e29c-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="2e29c-119">IID</span><span class="sxs-lookup"><span data-stu-id="2e29c-119">IID</span></span><br/>     | <span data-ttu-id="2e29c-120">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2e29c-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="2e29c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e29c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e29c-122">**Oggetto Installer**</span><span class="sxs-lookup"><span data-stu-id="2e29c-122">**Installer Object**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="2e29c-123">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="2e29c-123">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




