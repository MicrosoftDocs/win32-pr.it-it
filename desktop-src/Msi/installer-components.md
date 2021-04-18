---
description: La proprietà componenti di sola lettura restituisce un oggetto String enumerando il set di componenti installati per tutti i prodotti.
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: Proprietà Installer. Components
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Components
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6767be5182b15836c071bf8b00ed8441f6031dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330498"
---
# <a name="installercomponents-property"></a><span data-ttu-id="34894-103">Proprietà Installer. Components</span><span class="sxs-lookup"><span data-stu-id="34894-103">Installer.Components property</span></span>

<span data-ttu-id="34894-104">La proprietà **componenti** di sola lettura restituisce un oggetto [**String**](stringlist-object.md) enumerando il set di componenti installati per tutti i prodotti.</span><span class="sxs-lookup"><span data-stu-id="34894-104">The read-only **Components** property returns a [**StringList**](stringlist-object.md) object enumerating the set of installed components for all products.</span></span>

<span data-ttu-id="34894-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="34894-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="34894-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34894-106">Syntax</span></span>


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a><span data-ttu-id="34894-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="34894-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="34894-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="34894-108">Remarks</span></span>

<span data-ttu-id="34894-109">Per enumerare i componenti, un'applicazione è in grado di scorrere l'oggetto [**String**](stringlist-object.md) con un oggetto per ogni costrutto.</span><span class="sxs-lookup"><span data-stu-id="34894-109">To enumerate the components, an application can iterate through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="34894-110">Poiché i componenti non sono ordinati, eventuali nuovi componenti hanno un indice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="34894-110">Because components are not ordered, any new components has an arbitrary index.</span></span> <span data-ttu-id="34894-111">Ciò significa che la funzione può restituire componenti in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="34894-111">This means that the function can return components in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="34894-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34894-112">Requirements</span></span>



| <span data-ttu-id="34894-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="34894-113">Requirement</span></span> | <span data-ttu-id="34894-114">Valore</span><span class="sxs-lookup"><span data-stu-id="34894-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34894-115">Versione</span><span class="sxs-lookup"><span data-stu-id="34894-115">Version</span></span><br/> | <span data-ttu-id="34894-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="34894-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="34894-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="34894-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="34894-118">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="34894-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="34894-119">DLL</span><span class="sxs-lookup"><span data-stu-id="34894-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="34894-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34894-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="34894-121">IID</span><span class="sxs-lookup"><span data-stu-id="34894-121">IID</span></span><br/>     | <span data-ttu-id="34894-122">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="34894-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="34894-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34894-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34894-124">**MsiEnumComponents**</span><span class="sxs-lookup"><span data-stu-id="34894-124">**MsiEnumComponents**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




