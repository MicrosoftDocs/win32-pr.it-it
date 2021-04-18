---
description: Restituisce un oggetto di record che enumera l'elenco di prodotti.
ms.assetid: 30735b9f-091b-4915-9b07-9688c9be2d26
title: Proprietà Installer. ProductsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17d5e8290ab61b85fa8269f8b23f3cdabd30e012
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329131"
---
# <a name="installerproductsex-property"></a><span data-ttu-id="917ee-103">Proprietà Installer. ProductsEx</span><span class="sxs-lookup"><span data-stu-id="917ee-103">Installer.ProductsEx property</span></span>

<span data-ttu-id="917ee-104">La proprietà **ProductsEx** [**restituisce un oggetto**](recordlist-object.md) recordset che enumera l'elenco di prodotti.</span><span class="sxs-lookup"><span data-stu-id="917ee-104">The **ProductsEx** property returns a [**RecordList**](recordlist-object.md) object that enumerates the list of products.</span></span> <span data-ttu-id="917ee-105">Questa proprietà chiama [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa).</span><span class="sxs-lookup"><span data-stu-id="917ee-105">This property calls [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa).</span></span>

<span data-ttu-id="917ee-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="917ee-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="917ee-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="917ee-107">Syntax</span></span>


```JScript
propVal = Installer.ProductsEx
```



## <a name="property-value"></a><span data-ttu-id="917ee-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="917ee-108">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="917ee-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="917ee-109">Requirements</span></span>



| <span data-ttu-id="917ee-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="917ee-110">Requirement</span></span> | <span data-ttu-id="917ee-111">Valore</span><span class="sxs-lookup"><span data-stu-id="917ee-111">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="917ee-112">Versione</span><span class="sxs-lookup"><span data-stu-id="917ee-112">Version</span></span><br/> | <span data-ttu-id="917ee-113">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="917ee-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="917ee-114">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="917ee-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="917ee-115">Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="917ee-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="917ee-116">DLL</span><span class="sxs-lookup"><span data-stu-id="917ee-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="917ee-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="917ee-117"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="917ee-118">IID</span><span class="sxs-lookup"><span data-stu-id="917ee-118">IID</span></span><br/>     | <span data-ttu-id="917ee-119">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="917ee-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="917ee-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="917ee-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="917ee-121">**Programma di installazione**</span><span class="sxs-lookup"><span data-stu-id="917ee-121">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="917ee-122">**MsiEnumProductsEx**</span><span class="sxs-lookup"><span data-stu-id="917ee-122">**MsiEnumProductsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="917ee-123">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="917ee-123">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="917ee-124">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="917ee-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




