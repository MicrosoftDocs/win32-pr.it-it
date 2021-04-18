---
description: Il metodo SourceListClearSource rimuove un'origine di rete o URL. Accetta il tipo, il tipo di origine e SourcePath, il percorso di origine, come parametri da rimuovere. Questo metodo chiama MsiSourceListClearSource.
ms.assetid: a55676d4-795d-4ffe-8621-ef47c16a936c
title: Metodo Product. SourceListClearSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4988d0ba9003e087b6aeac58ae5587727067e01c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325880"
---
# <a name="productsourcelistclearsource-method"></a><span data-ttu-id="e7aca-105">Metodo Product. SourceListClearSource</span><span class="sxs-lookup"><span data-stu-id="e7aca-105">Product.SourceListClearSource method</span></span>

<span data-ttu-id="e7aca-106">Il metodo **SourceListClearSource** rimuove un'origine di rete o URL.</span><span class="sxs-lookup"><span data-stu-id="e7aca-106">The **SourceListClearSource** method removes a network or URL source.</span></span> <span data-ttu-id="e7aca-107">Accetta il *tipo*, il tipo di origine e *SourcePath*, il percorso di origine, come parametri da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e7aca-107">Accepts *Type*, the source type, and *SourcePath*, the source path, as parameters to be removed.</span></span> <span data-ttu-id="e7aca-108">Questo metodo chiama [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span><span class="sxs-lookup"><span data-stu-id="e7aca-108">This method calls the [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7aca-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7aca-109">Syntax</span></span>


```JScript
Product.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a><span data-ttu-id="e7aca-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7aca-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7aca-111">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="e7aca-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="e7aca-112">Tipo di origine da rimuovere: MSISOURCETYPE \_ Network o MSISOURCETYPE \_ URL.</span><span class="sxs-lookup"><span data-stu-id="e7aca-112">Type of source to be removed: MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> <dt>

<span data-ttu-id="e7aca-113">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="e7aca-113">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="e7aca-114">Percorso dell'origine da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e7aca-114">Path to the source to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7aca-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7aca-115">Return value</span></span>

<span data-ttu-id="e7aca-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e7aca-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7aca-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7aca-117">Requirements</span></span>



| <span data-ttu-id="e7aca-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7aca-118">Requirement</span></span> | <span data-ttu-id="e7aca-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e7aca-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7aca-120">Versione</span><span class="sxs-lookup"><span data-stu-id="e7aca-120">Version</span></span><br/> | <span data-ttu-id="e7aca-121">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e7aca-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e7aca-122">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e7aca-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e7aca-123">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e7aca-123">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="e7aca-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e7aca-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="e7aca-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7aca-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="e7aca-126">IID</span><span class="sxs-lookup"><span data-stu-id="e7aca-126">IID</span></span><br/>     | <span data-ttu-id="e7aca-127">IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e7aca-127">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="e7aca-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7aca-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7aca-129">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="e7aca-129">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="e7aca-130">**MsiSourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="e7aca-130">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="e7aca-131">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="e7aca-131">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




