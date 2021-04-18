---
description: La proprietà PatchesEx restituisce un oggetto recordset che enumera l'elenco di patch.
ms.assetid: 14fa0a1b-325c-42b7-b023-cd168e0615cc
title: Proprietà Installer. PatchesEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchesEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e615a9d17dbf1a40332afc5b49b3c0c5446963ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325291"
---
# <a name="installerpatchesex-property"></a><span data-ttu-id="d6557-103">Proprietà Installer. PatchesEx</span><span class="sxs-lookup"><span data-stu-id="d6557-103">Installer.PatchesEx property</span></span>

<span data-ttu-id="d6557-104">La proprietà **PatchesEx** restituisce un [**oggetto recordset**](recordlist-object.md) che enumera l'elenco di patch.</span><span class="sxs-lookup"><span data-stu-id="d6557-104">The **PatchesEx** property returns a [**RecordList**](recordlist-object.md) object that enumerates the list of patches.</span></span> <span data-ttu-id="d6557-105">Questa proprietà chiama [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span><span class="sxs-lookup"><span data-stu-id="d6557-105">This property calls [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span></span>

<span data-ttu-id="d6557-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d6557-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6557-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6557-107">Syntax</span></span>


```JScript
propVal = Installer.PatchesEx
```



## <a name="property-value"></a><span data-ttu-id="d6557-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d6557-108">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="d6557-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6557-109">Requirements</span></span>



| <span data-ttu-id="d6557-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6557-110">Requirement</span></span> | <span data-ttu-id="d6557-111">Valore</span><span class="sxs-lookup"><span data-stu-id="d6557-111">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6557-112">Versione</span><span class="sxs-lookup"><span data-stu-id="d6557-112">Version</span></span><br/> | <span data-ttu-id="d6557-113">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d6557-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d6557-114">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d6557-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d6557-115">Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6557-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="d6557-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d6557-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="d6557-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6557-117"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="d6557-118">IID</span><span class="sxs-lookup"><span data-stu-id="d6557-118">IID</span></span><br/>     | <span data-ttu-id="d6557-119">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d6557-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="d6557-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6557-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6557-121">**Programma di installazione**</span><span class="sxs-lookup"><span data-stu-id="d6557-121">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="d6557-122">**MsiEnumPatchesEx**</span><span class="sxs-lookup"><span data-stu-id="d6557-122">**MsiEnumPatchesEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[<span data-ttu-id="d6557-123">**Patch**</span><span class="sxs-lookup"><span data-stu-id="d6557-123">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="d6557-124">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="d6557-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




