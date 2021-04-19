---
description: La proprietà patch di sola lettura dell'oggetto Installer restituisce un oggetto String che contiene tutte le patch applicate al prodotto.
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: Proprietà Installer. Patches
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Patches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fd94c5853b3e455cf4d814dfb3c4078705ac727b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332176"
---
# <a name="installerpatches-property"></a><span data-ttu-id="12ace-103">Proprietà Installer. Patches</span><span class="sxs-lookup"><span data-stu-id="12ace-103">Installer.Patches property</span></span>

<span data-ttu-id="12ace-104">La proprietà **patch** di sola lettura dell'oggetto [**Installer**](installer-object.md) restituisce un oggetto [**String**](stringlist-object.md) che contiene tutte le patch applicate al prodotto.</span><span class="sxs-lookup"><span data-stu-id="12ace-104">The read-only **Patches** property of the [**Installer**](installer-object.md) object returns a [**StringList**](stringlist-object.md) object that contains all the patches applied to the product.</span></span>

<span data-ttu-id="12ace-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="12ace-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="12ace-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12ace-106">Syntax</span></span>


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a><span data-ttu-id="12ace-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="12ace-107">Property value</span></span>

<span data-ttu-id="12ace-108">Specifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="12ace-108">Specifies the product code.</span></span>

## <a name="remarks"></a><span data-ttu-id="12ace-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="12ace-109">Remarks</span></span>

<span data-ttu-id="12ace-110">Per enumerare le patch, un'applicazione esegue l'iterazione dell'oggetto [**String**](stringlist-object.md) con un oggetto per ogni costrutto.</span><span class="sxs-lookup"><span data-stu-id="12ace-110">To enumerate the patches, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="12ace-111">Poiché le patch non sono ordinate, tutte le nuove patch hanno un indice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="12ace-111">Because patches are not ordered, any new patch has an arbitrary index.</span></span> <span data-ttu-id="12ace-112">Ciò significa che la funzione può restituire le patch in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="12ace-112">This means that the function can return patches in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="12ace-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12ace-113">Requirements</span></span>



| <span data-ttu-id="12ace-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="12ace-114">Requirement</span></span> | <span data-ttu-id="12ace-115">Valore</span><span class="sxs-lookup"><span data-stu-id="12ace-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12ace-116">Versione</span><span class="sxs-lookup"><span data-stu-id="12ace-116">Version</span></span><br/> | <span data-ttu-id="12ace-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="12ace-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="12ace-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="12ace-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="12ace-119">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="12ace-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="12ace-120">DLL</span><span class="sxs-lookup"><span data-stu-id="12ace-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="12ace-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12ace-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="12ace-122">IID</span><span class="sxs-lookup"><span data-stu-id="12ace-122">IID</span></span><br/>     | <span data-ttu-id="12ace-123">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="12ace-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="12ace-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12ace-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12ace-125">**MsiEnumPatches**</span><span class="sxs-lookup"><span data-stu-id="12ace-125">**MsiEnumPatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




