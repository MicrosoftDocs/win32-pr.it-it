---
description: La proprietà ComponentQualifiers è una proprietà di sola lettura che restituisce un oggetto String enumerando il set di qualificatori registrati per il componente specificato.
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: Proprietà Installer. ComponentQualifiers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentQualifiers
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e6f58850974eaa2021578f0d56015ea0ef6d9e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329024"
---
# <a name="installercomponentqualifiers-property"></a><span data-ttu-id="afacd-103">Proprietà Installer. ComponentQualifiers</span><span class="sxs-lookup"><span data-stu-id="afacd-103">Installer.ComponentQualifiers property</span></span>

<span data-ttu-id="afacd-104">La proprietà **ComponentQualifiers** è una proprietà di sola lettura che restituisce un oggetto [**String**](stringlist-object.md) enumerando il set di qualificatori registrati per il componente specificato.</span><span class="sxs-lookup"><span data-stu-id="afacd-104">The **ComponentQualifiers** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of registered qualifiers for the specified component.</span></span>

<span data-ttu-id="afacd-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="afacd-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="afacd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afacd-106">Syntax</span></span>


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a><span data-ttu-id="afacd-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="afacd-107">Property value</span></span>

<span data-ttu-id="afacd-108">GUID di stringa che rappresenta la categoria di [componenti](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="afacd-108">A string GUID that represents the category of [component](publishcomponent-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="afacd-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="afacd-109">Remarks</span></span>

<span data-ttu-id="afacd-110">Per enumerare i qualificatori, l'applicazione esegue l'iterazione dell'oggetto [**String**](stringlist-object.md) con un oggetto per ogni costrutto.</span><span class="sxs-lookup"><span data-stu-id="afacd-110">To enumerate qualifiers the application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="afacd-111">Poiché i qualificatori non sono ordinati, qualsiasi nuovo qualificatore dispone di un indice arbitrario, ovvero la funzione può restituire qualificatori in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="afacd-111">Because qualifiers are not ordered, any new qualifier has an arbitrary index, meaning the function can return qualifiers in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="afacd-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afacd-112">Requirements</span></span>



| <span data-ttu-id="afacd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="afacd-113">Requirement</span></span> | <span data-ttu-id="afacd-114">Valore</span><span class="sxs-lookup"><span data-stu-id="afacd-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afacd-115">Versione</span><span class="sxs-lookup"><span data-stu-id="afacd-115">Version</span></span><br/> | <span data-ttu-id="afacd-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="afacd-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="afacd-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="afacd-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="afacd-118">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="afacd-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="afacd-119">DLL</span><span class="sxs-lookup"><span data-stu-id="afacd-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="afacd-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afacd-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="afacd-121">IID</span><span class="sxs-lookup"><span data-stu-id="afacd-121">IID</span></span><br/>     | <span data-ttu-id="afacd-122">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="afacd-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="afacd-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afacd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afacd-124">**MsiEnumComponentQualifiers**</span><span class="sxs-lookup"><span data-stu-id="afacd-124">**MsiEnumComponentQualifiers**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 




