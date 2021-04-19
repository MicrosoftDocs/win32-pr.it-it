---
description: La proprietà ProductInfo è una proprietà di sola lettura che restituisce il valore dell'attributo specificato per un prodotto installato o pubblicato.
ms.assetid: 144cbba7-ec2b-44cd-acc8-868c210ccebd
title: Proprietà Installer. ProductInfo (Oemupgex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 03ad741dd1c92fe68caccc4582738e54032750e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332943"
---
# <a name="installerproductinfo-property"></a><span data-ttu-id="9b51f-103">Proprietà Installer. ProductInfo</span><span class="sxs-lookup"><span data-stu-id="9b51f-103">Installer.ProductInfo property</span></span>

<span data-ttu-id="9b51f-104">La proprietà **ProductInfo** è una proprietà di sola lettura che restituisce il valore dell'attributo specificato per un prodotto installato o pubblicato.</span><span class="sxs-lookup"><span data-stu-id="9b51f-104">The **ProductInfo** property is a read-only property that returns the value of the specified attribute for an installed or published product.</span></span>

<span data-ttu-id="9b51f-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9b51f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b51f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b51f-106">Syntax</span></span>


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a><span data-ttu-id="9b51f-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9b51f-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="9b51f-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b51f-108">Remarks</span></span>

<span data-ttu-id="9b51f-109">La proprietà **ProductInfo** ("LocalPackage") non restituisce necessariamente un percorso al pacchetto memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="9b51f-109">The **ProductInfo** property ("LocalPackage") does not necessarily return a path to the cached package.</span></span> <span data-ttu-id="9b51f-110">Le installazioni in modalità manutenzione non devono essere richiamate da LocalPackage.</span><span class="sxs-lookup"><span data-stu-id="9b51f-110">Maintenance mode installations should be not be invoked from the LocalPackage.</span></span> <span data-ttu-id="9b51f-111">Il pacchetto memorizzato nella cache è solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="9b51f-111">The cached package is for internal uses only.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b51f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b51f-112">Requirements</span></span>



| <span data-ttu-id="9b51f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b51f-113">Requirement</span></span> | <span data-ttu-id="9b51f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9b51f-114">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b51f-115">Versione</span><span class="sxs-lookup"><span data-stu-id="9b51f-115">Version</span></span><br/> | <span data-ttu-id="9b51f-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9b51f-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9b51f-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9b51f-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9b51f-118">Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9b51f-118">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="9b51f-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b51f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9b51f-120"><dt>Oemupgex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b51f-120"><dt>Oemupgex.h</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="9b51f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="9b51f-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="9b51f-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b51f-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="9b51f-123">IID</span><span class="sxs-lookup"><span data-stu-id="9b51f-123">IID</span></span><br/>     | <span data-ttu-id="9b51f-124">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9b51f-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="9b51f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b51f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b51f-126">**MsiGetProductInfo**</span><span class="sxs-lookup"><span data-stu-id="9b51f-126">**MsiGetProductInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[<span data-ttu-id="9b51f-127">**MsiGetUserInfo**</span><span class="sxs-lookup"><span data-stu-id="9b51f-127">**MsiGetUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[<span data-ttu-id="9b51f-128">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="9b51f-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




