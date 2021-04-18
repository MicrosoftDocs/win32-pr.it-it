---
description: La proprietà Products è una proprietà di sola lettura che restituisce un oggetto String enumerando il set di tutti i prodotti installati o annunciati per l'utente e il computer correnti.
ms.assetid: 5c210827-a7cc-4358-bfe6-4d8e9767bd8c
title: Proprietà Installer. Products
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Products
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8d5b20a770154382e7e7a68cc3fe4d81c350fb1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328316"
---
# <a name="installerproducts-property"></a><span data-ttu-id="f63b7-103">Proprietà Installer. Products</span><span class="sxs-lookup"><span data-stu-id="f63b7-103">Installer.Products property</span></span>

<span data-ttu-id="f63b7-104">La proprietà **Products** è una proprietà di sola lettura che restituisce un oggetto [**String**](stringlist-object.md) enumerando il set di tutti i prodotti installati o annunciati per l'utente e il computer correnti.</span><span class="sxs-lookup"><span data-stu-id="f63b7-104">The **Products** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of all products installed or advertised for the current user and machine.</span></span>

<span data-ttu-id="f63b7-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f63b7-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f63b7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f63b7-106">Syntax</span></span>


```JScript
propVal = Installer.Products
```



## <a name="property-value"></a><span data-ttu-id="f63b7-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f63b7-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f63b7-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="f63b7-108">Remarks</span></span>

<span data-ttu-id="f63b7-109">Per enumerare i prodotti, un'applicazione esegue l'iterazione dell'oggetto [**String**](stringlist-object.md) con un oggetto per ogni costrutto.</span><span class="sxs-lookup"><span data-stu-id="f63b7-109">To enumerate the products, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="f63b7-110">Poiché i prodotti non sono ordinati, qualsiasi nuovo prodotto dispone di un indice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="f63b7-110">Because products are not ordered, any new product has an arbitrary index.</span></span> <span data-ttu-id="f63b7-111">Ciò significa che la funzione può restituire prodotti in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="f63b7-111">This means that the function can return products in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="f63b7-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f63b7-112">Requirements</span></span>



| <span data-ttu-id="f63b7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f63b7-113">Requirement</span></span> | <span data-ttu-id="f63b7-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f63b7-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f63b7-115">Versione</span><span class="sxs-lookup"><span data-stu-id="f63b7-115">Version</span></span><br/> | <span data-ttu-id="f63b7-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f63b7-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f63b7-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f63b7-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f63b7-118">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="f63b7-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f63b7-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f63b7-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="f63b7-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f63b7-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f63b7-121">IID</span><span class="sxs-lookup"><span data-stu-id="f63b7-121">IID</span></span><br/>     | <span data-ttu-id="f63b7-122">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f63b7-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="f63b7-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f63b7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f63b7-124">**MsiEnumProducts**</span><span class="sxs-lookup"><span data-stu-id="f63b7-124">**MsiEnumProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> </dl>

 

 




