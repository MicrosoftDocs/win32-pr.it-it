---
description: La proprietà Sources enumera tutte le origini per l'istanza del prodotto.
ms.assetid: 26602099-d0e0-4269-91d9-82943859811a
title: Product. Sources (proprietà)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a82363f6a61ebb9c441dfcfeeeafe3760e63c462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330623"
---
# <a name="productsources-property"></a><span data-ttu-id="17fd4-103">Product. Sources (proprietà)</span><span class="sxs-lookup"><span data-stu-id="17fd4-103">Product.Sources property</span></span>

<span data-ttu-id="17fd4-104">La proprietà **Sources** enumera tutte le origini per l'istanza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="17fd4-104">The **Sources** property enumerates all the sources for the product instance.</span></span> <span data-ttu-id="17fd4-105">Questa proprietà chiama [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) e restituisce la matrice di stringhe e accetta il tipo di origine come argomento.</span><span class="sxs-lookup"><span data-stu-id="17fd4-105">This property calls [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) and returns the array of strings, and accepts the source type as argument.</span></span> <span data-ttu-id="17fd4-106">Il tipo di origine può essere MSISOURCETYPE \_ Network o MSISOURCETYPE \_ URL.</span><span class="sxs-lookup"><span data-stu-id="17fd4-106">The source type can be MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

<span data-ttu-id="17fd4-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="17fd4-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="17fd4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17fd4-108">Syntax</span></span>


```JScript
propVal = Product.Sources
```



## <a name="property-value"></a><span data-ttu-id="17fd4-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="17fd4-109">Property value</span></span>

<span data-ttu-id="17fd4-110">Tipo di origine da enumerare.</span><span class="sxs-lookup"><span data-stu-id="17fd4-110">The type of source to enumerate.</span></span> <span data-ttu-id="17fd4-111">Il valore può essere *msiInstallSourceTypeNetwork* (1) o *msiInstallSourceTypeURL* (2).</span><span class="sxs-lookup"><span data-stu-id="17fd4-111">The value can be *msiInstallSourceTypeNetwork* (1) or *msiInstallSourceTypeURL* (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="17fd4-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17fd4-112">Requirements</span></span>



| <span data-ttu-id="17fd4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="17fd4-113">Requirement</span></span> | <span data-ttu-id="17fd4-114">Valore</span><span class="sxs-lookup"><span data-stu-id="17fd4-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17fd4-115">Versione</span><span class="sxs-lookup"><span data-stu-id="17fd4-115">Version</span></span><br/> | <span data-ttu-id="17fd4-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="17fd4-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="17fd4-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="17fd4-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="17fd4-118">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="17fd4-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="17fd4-119">DLL</span><span class="sxs-lookup"><span data-stu-id="17fd4-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="17fd4-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17fd4-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="17fd4-121">IID</span><span class="sxs-lookup"><span data-stu-id="17fd4-121">IID</span></span><br/>     | <span data-ttu-id="17fd4-122">IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="17fd4-122">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="17fd4-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17fd4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17fd4-124">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="17fd4-124">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="17fd4-125">**MsiSourceListEnumSources**</span><span class="sxs-lookup"><span data-stu-id="17fd4-125">**MsiSourceListEnumSources**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[<span data-ttu-id="17fd4-126">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="17fd4-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




