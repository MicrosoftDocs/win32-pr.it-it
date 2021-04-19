---
description: La proprietà ShortcutTarget dell'oggetto Installer esamina un collegamento e ne restituisce il prodotto, il nome della funzionalità e il componente, se disponibile.
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: Proprietà Installer. ShortcutTarget
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ShortcutTarget
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1c53d43188af9ed8f58ddd54916761e346f1bad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332166"
---
# <a name="installershortcuttarget-property"></a><span data-ttu-id="03293-103">Proprietà Installer. ShortcutTarget</span><span class="sxs-lookup"><span data-stu-id="03293-103">Installer.ShortcutTarget property</span></span>

<span data-ttu-id="03293-104">La proprietà **ShortcutTarget** dell'oggetto [**Installer**](installer-object.md) esamina un collegamento e ne restituisce il prodotto, il nome della funzionalità e il componente, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="03293-104">The **ShortcutTarget** property of the [**Installer**](installer-object.md) object examines a shortcut and returns its product, feature name, and component if available.</span></span>

<span data-ttu-id="03293-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="03293-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="03293-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03293-106">Syntax</span></span>


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a><span data-ttu-id="03293-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="03293-107">Property value</span></span>

<span data-ttu-id="03293-108">Percorso completo e nome file per il file.</span><span class="sxs-lookup"><span data-stu-id="03293-108">Full path and file name for the file.</span></span>

## <a name="remarks"></a><span data-ttu-id="03293-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="03293-109">Remarks</span></span>

<span data-ttu-id="03293-110">ShortcutTarget restituisce un [**oggetto record**](record-object.md) che contiene tre campi:</span><span class="sxs-lookup"><span data-stu-id="03293-110">ShortcutTarget returns a [**Record object**](record-object.md) that contains three fields:</span></span>

-   <span data-ttu-id="03293-111">Field 1 è un GUID per il codice prodotto del collegamento, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="03293-111">Field 1 is a GUID for the product code of the shortcut, if available.</span></span> <span data-ttu-id="03293-112">Questo campo può essere null.</span><span class="sxs-lookup"><span data-stu-id="03293-112">This field can be null.</span></span>
-   <span data-ttu-id="03293-113">Il campo 2 è l'ID funzionalità del collegamento, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="03293-113">Field 2 is the Feature ID of the shortcut, if available.</span></span> <span data-ttu-id="03293-114">Questo campo può essere null.</span><span class="sxs-lookup"><span data-stu-id="03293-114">This field can be null.</span></span>
-   <span data-ttu-id="03293-115">Il campo 3 è un GUID per il codice componente, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="03293-115">Field 3 is a GUID for the component code, if available.</span></span> <span data-ttu-id="03293-116">Questo campo può essere null.</span><span class="sxs-lookup"><span data-stu-id="03293-116">This field can be null.</span></span>

## <a name="requirements"></a><span data-ttu-id="03293-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03293-117">Requirements</span></span>



| <span data-ttu-id="03293-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="03293-118">Requirement</span></span> | <span data-ttu-id="03293-119">Valore</span><span class="sxs-lookup"><span data-stu-id="03293-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03293-120">Versione</span><span class="sxs-lookup"><span data-stu-id="03293-120">Version</span></span><br/> | <span data-ttu-id="03293-121">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="03293-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="03293-122">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="03293-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="03293-123">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="03293-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="03293-124">DLL</span><span class="sxs-lookup"><span data-stu-id="03293-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="03293-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03293-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="03293-126">IID</span><span class="sxs-lookup"><span data-stu-id="03293-126">IID</span></span><br/>     | <span data-ttu-id="03293-127">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="03293-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="03293-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03293-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03293-129">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="03293-129">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[<span data-ttu-id="03293-130">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="03293-130">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




