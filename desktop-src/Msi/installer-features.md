---
description: La proprietà features è una proprietà di sola lettura che restituisce un oggetto String enumerando il set di funzionalità pubblicate per il prodotto specificato.
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: Proprietà Installer. Features
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Features
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4f63ce80249fb8bd24d70f92e72c44420a13d798
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324638"
---
# <a name="installerfeatures-property"></a><span data-ttu-id="1fa01-103">Proprietà Installer. Features</span><span class="sxs-lookup"><span data-stu-id="1fa01-103">Installer.Features property</span></span>

<span data-ttu-id="1fa01-104">La proprietà **features** è una proprietà di sola lettura che restituisce un oggetto [**String**](stringlist-object.md) enumerando il set di funzionalità pubblicate per il prodotto specificato.</span><span class="sxs-lookup"><span data-stu-id="1fa01-104">The **Features** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of published features for the specified product.</span></span>

<span data-ttu-id="1fa01-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1fa01-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa01-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1fa01-106">Syntax</span></span>


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a><span data-ttu-id="1fa01-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1fa01-107">Property value</span></span>

<span data-ttu-id="1fa01-108">Specifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="1fa01-108">Specifies the product code of the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fa01-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="1fa01-109">Remarks</span></span>

<span data-ttu-id="1fa01-110">Per enumerare le funzionalità, un'applicazione esegue l'iterazione dell'oggetto [**String**](stringlist-object.md) con un oggetto per ogni costrutto.</span><span class="sxs-lookup"><span data-stu-id="1fa01-110">To enumerate the features, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="1fa01-111">Poiché le funzionalità non sono ordinate, qualsiasi nuova funzionalità dispone di un indice arbitrario, ovvero la funzione può restituire le funzionalità in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="1fa01-111">Because features are not ordered, any new feature has an arbitrary index, meaning the function can return features in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fa01-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fa01-112">Requirements</span></span>



| <span data-ttu-id="1fa01-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fa01-113">Requirement</span></span> | <span data-ttu-id="1fa01-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1fa01-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa01-115">Versione</span><span class="sxs-lookup"><span data-stu-id="1fa01-115">Version</span></span><br/> | <span data-ttu-id="1fa01-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1fa01-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1fa01-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1fa01-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1fa01-118">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="1fa01-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1fa01-119">DLL</span><span class="sxs-lookup"><span data-stu-id="1fa01-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="1fa01-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fa01-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1fa01-121">IID</span><span class="sxs-lookup"><span data-stu-id="1fa01-121">IID</span></span><br/>     | <span data-ttu-id="1fa01-122">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1fa01-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="1fa01-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1fa01-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa01-124">**MsiEnumFeatures**</span><span class="sxs-lookup"><span data-stu-id="1fa01-124">**MsiEnumFeatures**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[<span data-ttu-id="1fa01-125">Funzioni di stato del sistema</span><span class="sxs-lookup"><span data-stu-id="1fa01-125">System Status Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




