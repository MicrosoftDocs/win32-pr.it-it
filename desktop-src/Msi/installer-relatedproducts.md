---
description: La proprietà RelatedProducts di sola lettura restituisce un oggetto String enumerando il set di tutti i prodotti installati o annunciati per l'utente e il computer correnti con una proprietà UpgradeCode specificata nella tabella delle proprietà.
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: Proprietà Installer. RelatedProducts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RelatedProducts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fb30be6ea5250a90ef8aa18065e9be679946e503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332167"
---
# <a name="installerrelatedproducts-property"></a><span data-ttu-id="bbb0f-103">Proprietà Installer. RelatedProducts</span><span class="sxs-lookup"><span data-stu-id="bbb0f-103">Installer.RelatedProducts property</span></span>

<span data-ttu-id="bbb0f-104">La proprietà **RelatedProducts** di sola lettura restituisce un oggetto [**String**](stringlist-object.md) enumerando il set di tutti i prodotti installati o annunciati per l'utente e il computer correnti con una proprietà [**UpgradeCode**](upgradecode.md) specificata nella [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="bbb0f-104">The read-only **RelatedProducts** property returns a [**StringList**](stringlist-object.md) object enumerating the set of all products installed or advertised for the current user and machine with a specified [**UpgradeCode**](upgradecode.md) property in their [Property table](property-table.md).</span></span>

<span data-ttu-id="bbb0f-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="bbb0f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbb0f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbb0f-106">Syntax</span></span>


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a><span data-ttu-id="bbb0f-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bbb0f-107">Property value</span></span>

<span data-ttu-id="bbb0f-108">Codice di aggiornamento dei prodotti correlati enumerati dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="bbb0f-108">The upgrade code of related products that the installer enumerates.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbb0f-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbb0f-109">Remarks</span></span>

<span data-ttu-id="bbb0f-110">Per enumerare i prodotti correlati, un'applicazione scorre la [**stringa**](stringlist-object.md) usando un oggetto per ogni costrutto.</span><span class="sxs-lookup"><span data-stu-id="bbb0f-110">To enumerate the related products, an application iterates through the [**StringList**](stringlist-object.md) using a For Each construct.</span></span> <span data-ttu-id="bbb0f-111">Poiché i prodotti correlati non sono ordinati, qualsiasi nuovo prodotto correlato ha un indice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="bbb0f-111">Because related products are not ordered, any new related product has an arbitrary index.</span></span> <span data-ttu-id="bbb0f-112">Ciò significa che la funzione può restituire prodotti correlati in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="bbb0f-112">This means that the function can return related products in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbb0f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbb0f-113">Requirements</span></span>



| <span data-ttu-id="bbb0f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbb0f-114">Requirement</span></span> | <span data-ttu-id="bbb0f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bbb0f-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbb0f-116">Versione</span><span class="sxs-lookup"><span data-stu-id="bbb0f-116">Version</span></span><br/> | <span data-ttu-id="bbb0f-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bbb0f-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bbb0f-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bbb0f-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bbb0f-119">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="bbb0f-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="bbb0f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="bbb0f-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="bbb0f-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbb0f-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="bbb0f-122">IID</span><span class="sxs-lookup"><span data-stu-id="bbb0f-122">IID</span></span><br/>     | <span data-ttu-id="bbb0f-123">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bbb0f-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="bbb0f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbb0f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbb0f-125">**MsiEnumRelatedProducts**</span><span class="sxs-lookup"><span data-stu-id="bbb0f-125">**MsiEnumRelatedProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




