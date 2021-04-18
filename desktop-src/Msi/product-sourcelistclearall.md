---
description: Metodo SourceListClearAll. l'oggetto prodotto rimuove tutte le origini per il prodotto. È possibile specificare il tipo di origine da rimuovere.
ms.assetid: c8a63b54-7be6-424a-8653-0182b561faab
title: Metodo Product. SourceListClearAll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c921bd45b1acbac40444e4d11bb67d589149c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325883"
---
# <a name="productsourcelistclearall-method"></a><span data-ttu-id="bdecf-104">Metodo Product. SourceListClearAll</span><span class="sxs-lookup"><span data-stu-id="bdecf-104">Product.SourceListClearAll method</span></span>

<span data-ttu-id="bdecf-105">Metodo **SourceListClearAll** . l'oggetto [**prodotto**](product-object.md) rimuove tutte le origini per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="bdecf-105">The **SourceListClearAll** method the [**Product**](product-object.md) object removes all sources for the product.</span></span> <span data-ttu-id="bdecf-106">È possibile specificare il tipo di origine da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="bdecf-106">The type of source to remove can be specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdecf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdecf-107">Syntax</span></span>


```JScript
Product.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a><span data-ttu-id="bdecf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bdecf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdecf-109">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="bdecf-109">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="bdecf-110">Tipo di origine da rimuovere: MSISOURCETYPE \_ media, MSISOURCETYPE \_ Network o MSISOURCETYPE \_ URL.</span><span class="sxs-lookup"><span data-stu-id="bdecf-110">Type of source to be removed: MSISOURCETYPE\_MEDIA, MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdecf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bdecf-111">Return value</span></span>

<span data-ttu-id="bdecf-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bdecf-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdecf-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdecf-113">Requirements</span></span>



| <span data-ttu-id="bdecf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdecf-114">Requirement</span></span> | <span data-ttu-id="bdecf-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bdecf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdecf-116">Versione</span><span class="sxs-lookup"><span data-stu-id="bdecf-116">Version</span></span><br/> | <span data-ttu-id="bdecf-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bdecf-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bdecf-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bdecf-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bdecf-119">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="bdecf-119">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="bdecf-120">DLL</span><span class="sxs-lookup"><span data-stu-id="bdecf-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="bdecf-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdecf-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="bdecf-122">IID</span><span class="sxs-lookup"><span data-stu-id="bdecf-122">IID</span></span><br/>     | <span data-ttu-id="bdecf-123">IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bdecf-123">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="bdecf-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdecf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdecf-125">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="bdecf-125">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="bdecf-126">**MsiSourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="bdecf-126">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="bdecf-127">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="bdecf-127">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




